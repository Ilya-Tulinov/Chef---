# Chef installing the agent
Welcome to the Chef--- wiki! Linux Быстрая установка/переустановка агента делается с сервера chef от рута/иного где настроен knife, в примере тестовое имя hostname.oel.ru

#добавляем только пользователей yes|knife bootstrap hostname.oel.ru -N hostname.oel.ru -r "recipe[users::create_cto]" -E _default -x root -P rootxxx

#ИЛИ

#добавляем сразу all_nodes_role yes|knife bootstrap hostname.oel.ru -N hostname.oel.ru -r "role[all_nodes_role]" -E _default -x root -P rootxxx

#Если надо - добавляем общее далее. #1 - список рецептов для запуска, см. chef node show knife node run_list hostname.oel.ru "role[all_nodes_role]"

#2 - окружение - тот же набор рецептов для запуска и переменных на замену штатным knife node environment set hostname.oel.ru _default
