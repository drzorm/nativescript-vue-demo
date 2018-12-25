<template>
  <Page>
    <!-- <ActionBar title="Welcome to NativeScript-Vue!"/> -->
    <!-- <ActionBar flat="true">
      <StackLayout orientation="horizontal">
        <Image src="res://logo" width="25" height="25" verticalAlignment="center"/>
        <Label text="NativeScript" fontSize="24" verticalAlignment="center"/>
        <Image src="res://logo" width="25" height="25" verticalAlignment="center"/>
      </StackLayout>
    </ActionBar>-->
    <ActionBar title="My App">
      <NavigationButton text="Go back" android.systemIcon="ic_menu_back" @tap="goBack"/>
      <ActionItem
        @tap="onTapShare"
        ios.systemIcon="9"
        ios.position="left"
        android.systemIcon="ic_menu_share"
        android.position="actionBar"
      />
      <ActionItem
        @tap="onTapDelete"
        ios.systemIcon="16"
        ios.position="right"
        text="delete"
        android.position="popup"
      />
    </ActionBar>
    <!-- <AbsoluteLayout backgroundColor="#3c495e">
      <Label text="10,10" left="10" top="10" width="100" height="100" backgroundColor="#43b883"/>
      <Label text="120,10" left="120" top="10" width="100" height="100" backgroundColor="#43b883"/>
      <Label text="10,120" left="10" top="120" width="100" height="100" backgroundColor="#43b883"/>
      <Label
        text="120,120"
        left="120"
        top="120"
        width="100"
        height="100"
        backgroundColor="#43b883"
      />
    </AbsoluteLayout>-->
    <!-- <DockLayout stretchLastChild="false" backgroundColor="#3c495e">
      <Label text="left" dock="left" width="40" backgroundColor="#43b883"/>
      <Label text="top" dock="top" height="40" backgroundColor="#289062"/>
      <Label text="right" dock="right" width="40" backgroundColor="#43b883"/>
      <Label text="bottom" dock="bottom" height="40" backgroundColor="#289062"/>
    </DockLayout>-->
    <!-- <FlexboxLayout
      flexDirection="column-reverse"
      justifyContent="space-around"
      backgroundColor="#3c495e"
    >
      <Label text="first" height="70" backgroundColor="#43b883"/>
      <Label text="second" alignSelf="center" width="70" height="70" backgroundColor="#1c6b48"/>
      <Label
        text="third\nflex-end"
        alignSelf="flex-end"
        width="70"
        height="70"
        backgroundColor="#289062"
      />
      <Label text="fourth" height="70" backgroundColor="#289062"/>
    </FlexboxLayout>-->
    <!-- <GridLayout columns="40, auto, *" rows="40, auto, *" backgroundColor="#3c495e">
      <Label text="0,0" row="0" col="0" backgroundColor="#43b883"/>
      <Label text="0,1" row="0" col="1" colspan="2" backgroundColor="#1c6b48"/>
      <Label text="1,0" row="1" col="0" rowspan="2" backgroundColor="#289062"/>
      <Label text="1,1" row="1" col="1" backgroundColor="#43b883"/>
      <Label text="1,2" row="1" col="2" backgroundColor="#289062"/>
      <Label text="2,1" row="2" col="1" backgroundColor="#1c6b48"/>
      <Label text="2,2" row="2" col="2" backgroundColor="#43b883"/>
    </GridLayout>-->
    <!-- <StackLayout backgroundColor="#3c495e">
      <Label text="first" height="70" backgroundColor="#43b883"/>
      <Label text="second" height="70" backgroundColor="#289062"/>
      <Label text="third" height="70" backgroundColor="#1c6b48"/>
    </StackLayout>-->
    <!-- <WrapLayout backgroundColor="#3c495e">
      <Label text="first" width="30%" height="30%" backgroundColor="#43b883"/>
      <Label text="second" width="30%" height="30%" backgroundColor="#1c6b48"/>
      <Label text="third" width="30%" height="30%" backgroundColor="#289062"/>
      <Label text="fourth" width="30%" height="30%" backgroundColor="#289062"/>
    </WrapLayout>-->
    <StackLayout>
      <Button text="button" @tap="doSomething"/>
      <DatePicker day month year></DatePicker>
      <HtmlView html="<div><h1>HtmlView</h1></div>"/>
      <Image src="~/assets/images/NativeScript-Vue.png" stretch="none"/>
      <Label
        text="This is an overview of the most common usage of Label. For more information about the available properties, methods, or events, head over to the complete API documentation for Label."
        textWrap="true"
      />
      <Label textWrap="true">
        <FormattedString>
          <Span text="This text has a "/>
          <Span text="red " style="color: red"/>
          <Span text="piece of text. "/>
          <Span text="Also, this bit is italic, " fontStyle="italic"/>
          <Span text="and this bit is bold." fontWeight="bold"/>
        </FormattedString>
      </Label>

      <ActivityIndicator busy="true"/>
    </StackLayout>
  </Page>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {
    goBack() {
      alert('goBack');
    },
    onTapShare() {
      alert('onTapShare');
    },
    onTapDelete() {
      alert('onTapDelete');
    },
    doSomething() {
      alert('doSomething');
    }
  }
};
</script>

<style lang="less" scoped>
ActionBar {
  background-color: #53ba82;
  color: #ffffff;
}

.message {
  vertical-align: center;
  text-align: center;
  font-size: 20;
  color: #333333;
}
</style>
