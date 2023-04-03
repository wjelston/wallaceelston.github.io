### activity diagram.md

@startuml

    scale 1

    start
        :Add games to cart;
        :Checkout;
        :Check cookie;
        while (if cookie?) is (is invalid)
        :Show login form;
        endwhile
        fork
        :Mail invoice;
        fork again
        :Load games;
        end fork
        :Install and play;
    stop

@enduml