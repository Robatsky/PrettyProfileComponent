Pretty Profile Component 
========================
[![Current Version](https://img.shields.io/badge/version-1.0.0-green.svg)](https://github.com/IgorAntun/node-chat)

This is a JavaFX based storefront component for creating a modern looking user profile page.

---
### Inspiration 
This component is inspired by a forum post in the german forum [java-forum.org](https://www.java-forum.org/thema/loesungsvorschlaege-fuer-dieses-coole-control.185844/). 
Furthermore the design for this component comes from [Profile Page Inspiration](https://medium.muz.li/profile-page-inspiration-2152f16bde07).

---
### Features
---
### Usage

In order to use this you need to have at least Java 8 with JavaFX installed. Download the jar file and include it
into your project by putting it into the classpath.

You can either declare this component in your Java Code or in your FXML File. See the two following examples:
```Java
public class Main extends Application {
    @Override
    public void start(Stage primaryStage) throws Exception { 
        final PrettyProfileComponent ppc = FXMLLoader.load(getClass().getResource("/test.fxml"));

        primaryStage.setScene(new Scene(ppc, 1024, 800));
        primaryStage.show();
    }
}
```
```XML
<PrettyProfileComponent prefHeight="400.0" prefWidth="600.0" xmlns="http://javafx.com/javafx/8.0.172-ea" xmlns:fx="http://javafx.com/fxml/1">
    <nav>
        <HBox>
            <Label text="some title" />
            <Button text="Some Action" />
        </HBox>
    </nav>
    <profileContent>
        <ProfileContentWrapper>
            <sidebar>
                <VBox>
                    <Label alignment="CENTER" prefHeight="17.0" prefWidth="248.0" text="Sidebar">
                  <font>
                     <Font name="System Bold" size="15.0" />
                  </font></Label>
                    <Button contentDisplay="CENTER" prefHeight="25.0" prefWidth="239.0" text="Go To Profile" textAlignment="CENTER" />
                </VBox>
            </sidebar>
            <profileContent>
                <VBox>
                    <Label text="Content" />
                </VBox>
            </profileContent>
        </ProfileContentWrapper>
    </profileContent>
</PrettyProfileComponent>
```

---
### License
