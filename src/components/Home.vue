<template>
    <div class="container">
        <banner :language="language"/>
        <latest-articles :language="language"/>
        <link-button 
            :text="$t('Home.moreArticles')" 
            :link="`/${language.toLowerCase()}/articles`"
        />
        <our-story/>
        <link-button 
            :text="$t('Home.aboutLinkText')" 
            :link="`/${language.toLowerCase()}/about`"
        />
        <taste-our-coffee :language="language"/>
        <link-button 
            :text="$t('Home.cafesLinkText')" 
            :link="`/${language.toLowerCase()}/cafes`"
        />
    </div>
</template>

<script>
import Banner from './Banner'
import LatestArticles from './LatestArticles'
import LinkButton from './LinkButton'
import OurStory from './OurStory'
import TasteOurCoffee from './TasteOurCoffee'

export default {
  name: 'Home',
  props: ['language'],
  components: {
    Banner,
    LatestArticles,
    LinkButton,
    OurStory,
    TasteOurCoffee,
  },
}
</script>

