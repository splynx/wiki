<template lang="pug">
  .footer
    .container.container--1120.pre-footer-container
      div
        a.footer-logo(href='/')
          img(src='https://splynx.com/wp-content/uploads/2022/02/Logo.svg' alt='')
        p.footer-slogan ISP Billing and Network Management System
      .flex-grow-1
        .d-flex.menus-container.justify-content-space-between
          div
            h6 Product
            ul#menu-product.footer-menu
              li#menu-item-95.menu-item.menu-item-type-post_type.menu-item-object-page.menu-item-home.current-menu-item.page_item.page-item-14.current_page_item.menu-item-95
                a(href='https://splynx.com/' aria-current='page') Home
              li#menu-item-94.menu-item.menu-item-type-post_type.menu-item-object-page.menu-item-94
                a(href='https://splynx.com/pricing/') Pricing
              li#menu-item-2199.menu-item.menu-item-type-custom.menu-item-object-custom.menu-item-2199
                a(href='https://demo.splynx.com') Live demo
          div
            h6 Resources
            ul#menu-resourses.footer-menu
              li#menu-item-96.menu-item.menu-item-type-custom.menu-item-object-custom.menu-item-96
                a(href='https://wiki.splynx.com/') Knowledge base
              li#menu-item-97.menu-item.menu-item-type-custom.menu-item-object-custom.menu-item-97
                a(href='https://deploy.splynx.com/') Video tutorials
              li#menu-item-1826.menu-item.menu-item-type-post_type.menu-item-object-page.menu-item-1826
                a(href='https://splynx.com/blog/') Blog
              li#menu-item-100.menu-item.menu-item-type-custom.menu-item-object-custom.menu-item-100
                a(href='https://forum.splynx.com/') Forum
              li#menu-item-4184.menu-item.menu-item-type-post_type.menu-item-object-page.menu-item-4184
                a(href='https://splynx.com/release-notes-v-4-2/') Release notes
          div
            h6 Company
            ul#menu-company.footer-menu
              li#menu-item-101.menu-item.menu-item-type-post_type.menu-item-object-page.menu-item-101
                a(href='https://splynx.com/who-we-are/') Who we are
              li#menu-item-102.menu-item.menu-item-type-post_type.menu-item-object-page.menu-item-102
                a(href='https://splynx.com/contacts/') Contact us
              li#menu-item-2197.menu-item.menu-item-type-post_type.menu-item-object-page.menu-item-2197
                a(href='https://splynx.com/news/') News
          div
            h6 Connect with us
            ul.social
              li
                a(href='https://www.facebook.com/IspFramework' target='_blank')
                  img(src='https://splynx.com/wp-content/themes/Splynx/img/facebook.svg' alt='Facebook')
              li
                a(href='https://www.instagram.com/splynxframework' target='_blank')
                  img(src='https://splynx.com/wp-content/themes/Splynx/img/twitter.svg' alt='Twitter')
              li
                a(href='https://www.instagram.com/splynxframework' target='_blank')
                  img(src='https://splynx.com/wp-content/themes/Splynx/img/instagram.svg' alt='Instagram')
              li
                a(href='https://www.youtube.com/channel/UCQB0vydoC1LOqdheTPkxWpA' target='_blank')
                  img(src='https://splynx.com/wp-content/themes/Splynx/img/youtube.svg' alt='Youtube')
              li
                a(href='https://www.linkedin.com/company/splynx-isp-framework/' target='_blank')
                  img(src='https://splynx.com/wp-content/themes/Splynx/img/linkedin.svg' alt='Linkedin')
            .d-flex.mt-16._xs--mt-28.justify-content-start._xs--justify-content-center.hover_dropdown
              .title.d-flex.column-gap-16
              ul.list.up
    .container.container--1120.mt-60.footer-links
      .terms
        .copyright &copy; Splynx ISP Framework by Splynx s.r.o
        .right-links
          a(href='https://splynx.com/cookie-policy/') Cookies Policy
          a(href='https://splynx.com/privacy-policy/') Privacy Policy

</template>

<script>
import {get} from 'vuex-pathify'

export default {
  props: {
    color: {
      type: String,
      default: 'grey lighten-3'
    },
    darkColor: {
      type: String,
      default: 'grey darken-3'
    }
  },
  data() {
    return {
      currentYear: (new Date()).getFullYear()
    }
  },
  computed: {
    company: get('site/company'),
    contentLicense: get('site/contentLicense'),
    bgColor() {
      if (!this.$vuetify.theme.dark) {
        return this.color
      } else {
        return this.darkColor
      }
    }
  }
}
</script>

<style lang="scss">
.d-flex {
  display: flex;
}

.justify-content-space-between {
  justify-content: space-between;
}

.mt-60 {
  margin-top: 60px;
}

.footer {
  color: #1b2124;
  background: #fff;
  padding: 60px 0px 0px 256px;
  border-top:1px solid #e7e7e7;
  transition: .2s cubic-bezier(.4,0,.2,1);
}

.footer .footer-logo {
  display: flex
}

.footer .footer-slogan {
  margin-top: 12px;
  font-weight: 400;
  font-size: 14px;
  line-height: 24px;
  color: #6c757d
}

.footer .menus-container {
  margin-left: 90px;
  justify-content: space-between
}

.footer .terms {
  display: flex;
  justify-content: space-between;
  width: 100%
}

.footer .terms, .footer .terms a {
  color: #6c757d;
  font-size: 14px;
  line-height: 24px
}

.footer .terms .right-links a:not(:last-child) {
  margin-right: 28px
}

.footer .footer-menu {
  margin-bottom: -12px;
  padding: 0;
}

.footer li {
  list-style: none;
  margin: 12px 0
}

.footer a {
  color: #1b2124 !important;
  font-size: 16px;
  line-height: 24px;
  font-weight: 400;
  text-decoration: none;
}

.footer h6 {
  font-size: 16px;
  line-height: 24px;
  font-weight: 600
}

.footer ul.social {
  margin-top: 16px;
  display: flex;
  padding: 0;
}

.footer ul.social li {
  width: 18px;
  height: 18px;
  display: flex;
  align-items: center;
  margin: 0
}

.footer ul.social li:not(:last-child) {
  margin-right: 16px
}

.footer ul.social li a {
  width: 100%;
  height: 100%;
  display: flex;
  transition: .3s;
  transform: translateY(0)
}

.footer ul.social li a:hover {
  transform: translateY(-2px)
}

.footer ul.social li a img {
  width: 100%;
  height: 100%;
  object-fit: contain
}

.footer ul.social li a img path {
  fill: #367bf5
}

@media(min-width: 678px) and (max-width: 1200px) {
  .footer .pre-footer-container {
    flex-direction: column
  }

  .footer .pre-footer-container > div:first-child {
    margin-bottom: 60px
  }

  .footer .menus-container {
    display: grid;
    margin-left: 0;
    grid-row-gap: 24px;
    grid-template-columns: repeat(auto-fit, minmax(170px, 1fr))
  }
}

@media(max-width: 678px) {
  .footer {
    padding-top: 28px
  }

  .footer h6 {
    text-align: center;
    font-size: 20px;
    line-height: 24px;
    font-weight: 500
  }

  .footer ul.social {
    margin-top: 28px
  }

  .footer ul.social li {
    width: 32px;
    height: 32px
  }

  .footer ul.social li:not(:last-child) {
    margin-right: 32px
  }

  .footer .footer-logo {
    justify-content: center
  }

  .footer .footer-logo img {
    height: 28px
  }

  .footer .terms {
    align-items: center;
    flex-direction: column-reverse
  }

  .footer .footer-links {
    margin-top: 25px
  }

  .footer .pre-footer-container {
    flex-direction: column;
    align-items: center
  }

  .footer .menus-container {
    margin-left: 0
  }

  .footer .menus-container > div {
    margin-top: 40px
  }

  .footer .menus-container > div:not(:last-child) {
    display: none
  }

  .footer .right-links {
    font-size: 14px;
    display: flex;
    flex-direction: column
  }

  .footer .right-links a {
    font-size: 16px;
    text-align: center;
    margin-bottom: 20px
  }

  .footer .right-links a:not(:last-child) {
    margin-right: 0 !important
  }
}

.footer .container {
  display: flex;
  width: 100%;
  padding-left: 20px;
  padding-right: 20px;
  max-width: 100%;
}

.container--1120 {
  max-width: 100%;
}

@media (min-width: 1264px) {
  .container.container--1120 {
    max-width: 100%;
  }
}

@media (min-width: 960px) {
  .container.container--1120 {
    max-width: 100%;
  }
}

.footer ul.social {
  padding: 0;
}

@media (max-width: 960px) {
  .footer .container {
    max-width: 100%;
  }
  .footer{
    padding-left: 0 !important;
  }
}
</style>
