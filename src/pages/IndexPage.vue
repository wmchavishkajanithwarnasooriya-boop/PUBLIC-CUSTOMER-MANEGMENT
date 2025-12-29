<template>
  <q-page class="bg-grey-1">
    <!-- Hero Section -->
    <div class="hero-section relative-position flex flex-center text-white overflow-hidden">
      <div class="absolute-full bg-gradient-primary"></div>

      <!-- Decorative circles -->
      <div class="absolute-top-right q-mr-xl q-mt-xl opacity-20">
        <div class="circle-1"></div>
      </div>
      <div class="absolute-bottom-left q-ml-xl q-mb-xl opacity-20">
        <div class="circle-2"></div>
      </div>

      <div class="container relative-position z-top q-py-xl">
        <div class="row items-center q-col-gutter-xl">
          <!-- Left Content -->
          <div class="col-12 col-md-6 text-left">
            <q-badge
              color="white"
              text-color="primary"
              label="New V2.0 Released"
              class="q-mb-md q-py-xs q-px-sm text-weight-bold shadow-2 rounded-borders"
            />
            <h1 class="text-h3 text-md-h1 text-weight-bolder q-mb-md font-heading leading-tight">
              Manage Customers <br />
              Like a Pro.
            </h1>
            <p class="text-h6 text-grey-3 q-mb-xl" style="max-width: 500px">
              Experience the next generation of customer management. Powerful, intuitive, and
              designed for growth.
            </p>
            <div class="row q-gutter-md q-mb-xl">
              <q-btn
                unelevated
                color="white"
                text-color="primary"
                label="Start Free Trial"
                size="lg"
                no-caps
                class="q-px-xl text-weight-bold shadow-10 btn-hover"
              />
              <q-btn
                outline
                color="white"
                label="Watch Demo"
                size="lg"
                no-caps
                class="q-px-xl text-weight-bold btn-hover"
                icon="play_circle_filled"
              />
            </div>

            <div class="row q-gutter-lg opacity-80 text-subtitle2">
              <div class="row items-center">
                <q-icon name="check_circle" class="q-mr-sm" size="20px" /> No credit card required
              </div>
              <div class="row items-center">
                <q-icon name="check_circle" class="q-mr-sm" size="20px" /> 14-day free trial
              </div>
              <div class="row items-center">
                <q-icon name="check_circle" class="q-mr-sm" size="20px" /> Cancel anytime
              </div>
            </div>
          </div>

          <!-- Right Image -->
          <div class="col-12 col-md-6 flex flex-center">
            <div class="relative-position">
              <div
                class="absolute-center bg-white opacity-20"
                style="width: 100%; height: 100%; filter: blur(40px); transform: scale(0.9)"
              ></div>
              <img
                src="https://cdn.quasar.dev/img/parallax2.jpg"
                class="rounded-borders shadow-20"
                style="
                  width: 100%;
                  max-width: 600px;
                  transform: perspective(1000px) rotateY(-10deg) rotateX(5deg);
                  border: 2px solid rgba(255, 255, 255, 0.3);
                "
                alt="Dashboard Preview"
              />
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Features Section -->
    <div class="section-padding container">
      <div class="text-center q-mb-xl">
        <div class="text-primary text-weight-bold text-uppercase q-mb-sm tracking-wide">
          Why Choose Us
        </div>
        <h2 class="text-h3 text-weight-bold text-dark font-heading">
          Everything you need to scale
        </h2>
      </div>

      <div class="row q-col-gutter-lg">
        <div class="col-12 col-md-4" v-for="(feature, index) in features" :key="index">
          <q-card class="feature-card no-shadow border-gray q-pa-lg full-height column">
            <div
              class="q-mb-md flex flex-center bg-blue-1 rounded-borders"
              style="width: 60px; height: 60px"
            >
              <q-icon :name="feature.icon" color="primary" size="30px" />
            </div>
            <div class="text-h5 text-weight-bold text-dark q-mb-sm">{{ feature.title }}</div>
            <p class="text-grey-7">{{ feature.description }}</p>
          </q-card>
        </div>
      </div>
    </div>

    <!-- Stats Section -->
    <div class="bg-white q-py-xl border-top-gray">
      <div class="container row justify-center q-col-gutter-xl text-center">
        <div class="col-6 col-md-3">
          <div class="text-h3 text-weight-bolder text-primary">10k+</div>
          <div class="text-grey-6 text-subtitle1">Active Users</div>
        </div>
        <div class="col-6 col-md-3">
          <div class="text-h3 text-weight-bolder text-primary">99.9%</div>
          <div class="text-grey-6 text-subtitle1">Uptime</div>
        </div>
        <div class="col-6 col-md-3">
          <div class="text-h3 text-weight-bolder text-primary">24/7</div>
          <div class="text-grey-6 text-subtitle1">Support</div>
        </div>
      </div>
    </div>

    <!-- CTA Section -->
    <div class="container section-padding">
      <div
        class="bg-dark text-white rounded-xl q-pa-xl text-center relative-position overflow-hidden"
      >
        <div class="absolute-bottom-right opacity-10" style="bottom: -50px; right: -50px">
          <q-icon name="rocket_launch" size="300px" />
        </div>

        <div class="relative-position z-top">
          <h2 class="text-h3 text-weight-bold q-mb-md">Ready to get started?</h2>
          <p class="text-h6 text-grey-4 q-mb-lg max-w-600 q-mx-auto">
            Join thousands of satisfied customers who have transformed their business with our
            platform.
          </p>
          <q-btn
            unelevated
            color="primary"
            label="Create Free Account"
            size="lg"
            no-caps
            class="text-weight-bold q-px-xl shadow-4 btn-hover"
          />
        </div>
      </div>
    </div>
  </q-page>
</template>

<script setup>
const features = [
  {
    title: 'Smart Analytics',
    description:
      'Get deep insights into your customer base with our AI-powered analytics dashboard.',
    icon: 'analytics',
  },
  {
    title: 'Secure Data',
    description:
      'Enterprise-grade encryption keeps your customer data safe and compliant with global standards.',
    icon: 'security',
  },
  {
    title: 'Fast Integration',
    description:
      'Connect with your favorite tools in seconds with our extensive library of one-click integrations.',
    icon: 'bolt',
  },
  {
    title: 'Team Collaboration',
    description: 'Built for teams. Share insights, assign tasks, and work together seamlessly.',
    icon: 'groups',
  },
  {
    title: 'Automated Workflows',
    description:
      'Save time by automating repetitive tasks and focusing on what matters - your customers.',
    icon: 'settings_suggest',
  },
  {
    title: 'Mobile First',
    description:
      'Manage your business on the go with our fully responsive and powerful mobile interface.',
    icon: 'smartphone',
  },
]
</script>

<style lang="scss" scoped>
.hero-section {
  min-height: 85vh;
  // Fallback if gradient fails, but Quasar text-primary usually handles solid colors.
  // We define a custom gradient here.
}
.bg-gradient-primary {
  background: linear-gradient(135deg, #1976d2 0%, #0d47a1 100%);
  // Make it darker/richer
  background: linear-gradient(135deg, #2563eb 0%, #1e40af 100%);
}

.opacity-20 {
  opacity: 0.2;
}
.opacity-80 {
  opacity: 0.8;
}
.opacity-10 {
  opacity: 0.1;
}

.circle-1,
.circle-2 {
  width: 300px;
  height: 300px;
  border-radius: 50%;
  background: white;
  filter: blur(80px);
}

.font-heading {
  font-family: 'Inter', sans-serif; // Assuming you might add this or use system font
  letter-spacing: -1px;
}

.leading-tight {
  line-height: 1.1;
}

.max-w-600 {
  max-width: 600px;
}

.section-padding {
  padding: 100px 20px;
}

.feature-card {
  transition:
    transform 0.3s ease,
    box-shadow 0.3s ease;
  &:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 40px -10px rgba(0, 0, 0, 0.1);
  }
}

.border-gray {
  border: 1px solid #e2e8f0;
}
.border-top-gray {
  border-top: 1px solid #e2e8f0;
}

.btn-hover {
  transition: transform 0.2s;
  &:hover {
    transform: scale(1.05);
  }
}

.rounded-xl {
  border-radius: 24px;
}
</style>
