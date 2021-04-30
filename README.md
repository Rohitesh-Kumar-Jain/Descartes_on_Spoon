# Descartes_on_Spoon

This repository contains the pit report generated after running [Descartes](https://github.com/STAMP-project/pitest-descartes) on [Spoon](https://github.com/INRIA/spoon).


## How to view the pit-report?
To view the pit-report download this repo and then open [index.html](https://github.com/Rohitesh-Kumar-Jain/Descartes_on_Spoon/blob/master/202104291236/index.html) in your local server. 

![Screen Shot 2021-04-30 at 12 50 03-fullpage](https://user-images.githubusercontent.com/62026125/116661843-ab692680-a9b2-11eb-946f-439d6e1dd7aa.png)

## How many methods and tests does this report covers?
This report is generated using all the methods and tests in Spoon.

If you are looking for reports generated after running on subsets of methods and tests, check [this](https://github.com/Rohitesh-Kumar-Jain/Descartes_Pit_Reports).

## How can this report generated?

<img width="664" alt="Screenshot 2021-04-30 at 12 51 52 PM" src="https://user-images.githubusercontent.com/62026125/116662002-d94e6b00-a9b2-11eb-9919-c0766948e1b9.png">

To generate this report add this plugin in Spoon.

```
        <plugin>
            <groupId>org.pitest</groupId>
            <artifactId>pitest-maven</artifactId>
            <version>1.6.4</version>
            <configuration>
                <mutationEngine>descartes</mutationEngine>
                <targetClasses>
                    <param>spoon.compiler.*</param>
                    <param>spoon.experimental.*</param>
                    <param>spoon.javadoc.*</param>
                    <param>spoon.legacy.*</param>
                    <param>spoon.metamodel.*</param>
                    <param>spoon.pattern.*</param>
                    <param>spoon.refactoring.*</param>
                    <param>spoon.template.*</param>
                    <param>spoon.processing.*</param>
                    <param>spoon.reflect.*</param>
                    <param>spoon.support.*</param>
                    <param>spoon.testing.*</param>
                </targetClasses>
                <targetTests>
                    <param>spoon.*</param>
                </targetTests>
                <skipFailingTests>true</skipFailingTests>
            </configuration>
            <dependencies>
                <dependency>
                    <groupId>eu.stamp-project</groupId>
                    <artifactId>descartes</artifactId>
                    <version>1.3.1</version>
                </dependency>
            </dependencies>
        </plugin>
```
