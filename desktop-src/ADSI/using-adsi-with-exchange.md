---
title: Использование ADSI с Exchange
description: Для Exchange 2000 сведения об использовании ADSI с Exchange содержатся в пакете SDK для Exchange 2000. Дополнительные сведения см. в разделе задачи управления для ADSI.
ms.assetid: c806ca1b-c97c-4567-af8b-e12cfde2bf70
ms.tgt_platform: multiple
keywords:
- ADSI для Exchange ADSI
- ADSI для Exchange ADSI, почтовые ящики
- ADSI для Exchange ADSI, почтовые ящики, создание
- ADSI для Exchange ADSI, почтовые ящики, удаление
- ADSI для Exchange ADSI, почтовые ящики, Установка дескриптора безопасности на
- ADSI для Exchange ADSI, почтовые ящики, поиск домашнего сервера для
- ADSI для Exchange ADSI, получение и изменение сообщений
- ADSI для Exchange ADSI, дескрипторы безопасности
- ADSI для Exchange ADSI, дескрипторы безопасности, манипуляции
- ADSI для Exchange ADSI, дескрипторы безопасности, Настройка
- ADSI для Exchange ADSI, контейнер получателей
- ADSI для Exchange ADSI, Просмотр свойств объектов Exchange
- ADSI для Exchange ADSI, контейнер получателей, настраиваемый
- ADSI для Exchange ADSI, Exchange Server
- ADSI для Exchange ADSI, Exchange Server, просмотр и изменение схемы
- ADSI для Exchange ADSI, Exchange Server, листинг версии сервера
- ADSI для Exchange ADSI, Exchange Server, Организация и имя сайта
- ADSI для Exchange ADSI, Exchange Server, поиск домашнего сервера почтовых ящиков
- ADSI для Exchange ADSI, адреса электронной почты, получение
- ADSI для Exchange ADSI, списки рассылки, создание
- ADSI для Exchange ADSI, скрытые или удаленные записи
- ADSI для Exchange ADSI, извлечение изменений службы каталогов
- ADSI для Exchange ADSI, размер сообщения
- ADSI для Exchange ADSI, устранение неполадок
- почтовые ящики ADSI
- почтовые ящики ADSI, создание
- почтовые ящики ADSI, удаление
- почтовые ящики ADSI, Установка дескриптора безопасности на
- почтовые ящики ADSI, поиск домашнего сервера для
- сообщения ADSI, получение и изменение
- Exchange ADSI
- Exchange ADSI, почтовые ящики
- Exchange ADSI, почтовые ящики, создание
- Exchange ADSI, почтовые ящики, удаление
- Exchange ADSI, почтовые ящики, Установка дескриптора безопасности на
- Exchange ADSI, почтовые ящики, поиск домашнего сервера для
- Exchange ADSI, получение и изменение сообщений
- Exchange ADSI, дескрипторы безопасности
- Exchange ADSI, дескрипторы безопасности, манипуляции
- Exchange ADSI, дескрипторы безопасности, Настройка
- Exchange ADSI, контейнер получателей
- Exchange ADSI, Просмотр свойств объектов Exchange
- Exchange ADSI, контейнер получателей, Пользовательский
- Exchange ADSI, Exchange Server
- Exchange ADSI, Exchange Server, просмотр и изменение схемы
- Exchange ADSI, Exchange Server, листинг версии сервера
- Exchange ADSI, Exchange Server, Организация и имя сайта
- Exchange ADSI, Exchange Server, поиск домашнего сервера почтовых ящиков
- Exchange ADSI, адреса электронной почты, получение
- Exchange ADSI, списки рассылки, создание
- Exchange ADSI, скрытые или удаленные записи
- Exchange ADSI, получение изменений службы каталогов
- Exchange ADSI, размер сообщения
- Exchange ADSI, устранение неполадок
- дескрипторы безопасности ADSI, для объектов Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833d60c284a12e759eb74b22c9aa48abc75da463
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105654360"
---
# <a name="using-adsi-with-exchange"></a><span data-ttu-id="eb553-159">Использование ADSI с Exchange</span><span class="sxs-lookup"><span data-stu-id="eb553-159">Using ADSI with Exchange</span></span>

<span data-ttu-id="eb553-160">Для Exchange 2000 сведения об использовании ADSI с Exchange содержатся в пакете SDK для Exchange 2000.</span><span class="sxs-lookup"><span data-stu-id="eb553-160">For Exchange 2000, information for using ADSI with Exchange is contained in the Exchange 2000 SDK.</span></span> <span data-ttu-id="eb553-161">Дополнительные сведения см. в разделе [задачи управления для ADSI](/previous-versions/office/developer/exchange-server-2003/aa125368(v=exchg.65)).</span><span class="sxs-lookup"><span data-stu-id="eb553-161">For more information, see [Management Tasks for ADSI](/previous-versions/office/developer/exchange-server-2003/aa125368(v=exchg.65)).</span></span>

<span data-ttu-id="eb553-162">В этом разделе можно найти следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="eb553-162">The following tasks can be found in this section:</span></span>

-   <span data-ttu-id="eb553-163">Создание URL-адреса пользователя</span><span class="sxs-lookup"><span data-stu-id="eb553-163">Creating a user URL</span></span>
-   <span data-ttu-id="eb553-164">Создание путей Active Directory</span><span class="sxs-lookup"><span data-stu-id="eb553-164">Building Active Directory paths</span></span>
-   <span data-ttu-id="eb553-165">Перечисление серверов Exchange 2000 с помощью ADSI</span><span class="sxs-lookup"><span data-stu-id="eb553-165">Enumerating Exchange 2000 servers with ADSI</span></span>
-   <span data-ttu-id="eb553-166">Управление атрибутами расширения с помощью ADSI</span><span class="sxs-lookup"><span data-stu-id="eb553-166">Manipulating extension attributes with ADSI</span></span>
-   <span data-ttu-id="eb553-167">Добавление и удаление объекта Manager с помощью ADSI</span><span class="sxs-lookup"><span data-stu-id="eb553-167">Adding/removing a manager object with ADSI</span></span>
-   <span data-ttu-id="eb553-168">Перечисление свойств объектов Exchange с помощью ADSI/ADO</span><span class="sxs-lookup"><span data-stu-id="eb553-168">Enumerating Exchange object properties with ADSI/ADO</span></span>
-   <span data-ttu-id="eb553-169">Получение устаревшего различающегося имени Exchange с помощью ADSI</span><span class="sxs-lookup"><span data-stu-id="eb553-169">Retrieving a legacy Exchange distinguished name with ADSI</span></span>
-   <span data-ttu-id="eb553-170">Поиск имени организации Exchange с помощью ADSI</span><span class="sxs-lookup"><span data-stu-id="eb553-170">Finding the Exchange organization name using ADSI</span></span>
-   <span data-ttu-id="eb553-171">Поиск списков адресов Exchange с помощью ADSI</span><span class="sxs-lookup"><span data-stu-id="eb553-171">Finding Exchange address lists with ADSI</span></span>
-   <span data-ttu-id="eb553-172">Создание списка рассылки с помощью КДОЕКСМ и ADSI</span><span class="sxs-lookup"><span data-stu-id="eb553-172">Creating a distribution list using CDOEXM and ADSI</span></span>
-   <span data-ttu-id="eb553-173">Настройка ограничения для сообщений на виртуальном SMTP-сервере с помощью ADSI</span><span class="sxs-lookup"><span data-stu-id="eb553-173">Setting message restriction on an SMTP virtual server using ADSI</span></span>

<span data-ttu-id="eb553-174">Для Exchange 5,5 Справочник по ADSI и использование сведений можно найти в руководстве по использованию [ADSI Exchange](/previous-versions/office/developer/exchange-server-2007/aa579394(v=exchg.80)) .</span><span class="sxs-lookup"><span data-stu-id="eb553-174">For Exchange 5.5, the ADSI reference and using information can be found in the [ADSI Exchange](/previous-versions/office/developer/exchange-server-2007/aa579394(v=exchg.80)) guide.</span></span>

<span data-ttu-id="eb553-175">В этом разделе можно найти следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="eb553-175">The following tasks can be found in this section:</span></span>

-   <span data-ttu-id="eb553-176">Просмотр и изменение схемы Exchange Server</span><span class="sxs-lookup"><span data-stu-id="eb553-176">Viewing and modifying the Exchange Server Schema</span></span>
-   <span data-ttu-id="eb553-177">Просмотр необработанных свойств объекта Exchange</span><span class="sxs-lookup"><span data-stu-id="eb553-177">Viewing the raw properties of an Exchange object</span></span>
-   <span data-ttu-id="eb553-178">Создание почтового ящика Exchange</span><span class="sxs-lookup"><span data-stu-id="eb553-178">Creating an Exchange mailbox</span></span>
-   <span data-ttu-id="eb553-179">Установка дескриптора безопасности в почтовом ящике Exchange</span><span class="sxs-lookup"><span data-stu-id="eb553-179">Setting the security descriptor on an Exchange mailbox</span></span>
-   <span data-ttu-id="eb553-180">Управление дескрипторами безопасности и идентификаторами SID</span><span class="sxs-lookup"><span data-stu-id="eb553-180">Manipulating security descriptors and SIDs</span></span>
-   <span data-ttu-id="eb553-181">Удаление объекта почтового ящика</span><span class="sxs-lookup"><span data-stu-id="eb553-181">Deleting a mailbox object</span></span>
-   <span data-ttu-id="eb553-182">Создание пользовательского получателя</span><span class="sxs-lookup"><span data-stu-id="eb553-182">Creating a custom recipient</span></span>
-   <span data-ttu-id="eb553-183">Создание контейнера получателей</span><span class="sxs-lookup"><span data-stu-id="eb553-183">Creating a recipients container</span></span>
-   <span data-ttu-id="eb553-184">Получение имени Организации и сайта с сервера</span><span class="sxs-lookup"><span data-stu-id="eb553-184">Getting the organization and site name from a server</span></span>
-   <span data-ttu-id="eb553-185">Перечисление версии сервера Exchange Server всех серверов в Организации</span><span class="sxs-lookup"><span data-stu-id="eb553-185">Listing the Exchange server version of all the servers in the organization</span></span>
-   <span data-ttu-id="eb553-186">Поиск домашнего сервера почтового ящика</span><span class="sxs-lookup"><span data-stu-id="eb553-186">Finding the home server of a mailbox</span></span>
-   <span data-ttu-id="eb553-187">Получение адресов электронной почты</span><span class="sxs-lookup"><span data-stu-id="eb553-187">Retrieving email addresses</span></span>
-   <span data-ttu-id="eb553-188">Доступ к скрытым или удаленным записям</span><span class="sxs-lookup"><span data-stu-id="eb553-188">Accessing hidden or deleted entries</span></span>
-   <span data-ttu-id="eb553-189">Получение изменений, внесенных в службу каталогов</span><span class="sxs-lookup"><span data-stu-id="eb553-189">Retrieving changes made to the directory service</span></span>
-   <span data-ttu-id="eb553-190">Создание списка рассылки на основе результатов запроса</span><span class="sxs-lookup"><span data-stu-id="eb553-190">Creating a distribution list from the results of a query</span></span>
-   <span data-ttu-id="eb553-191">Получение или изменение размера сообщения</span><span class="sxs-lookup"><span data-stu-id="eb553-191">Getting or modifying message size</span></span>
-   <span data-ttu-id="eb553-192">Использование кодов ошибок LDAP для устранения неполадок</span><span class="sxs-lookup"><span data-stu-id="eb553-192">Using LDAP error codes to troubleshoot problems</span></span>

 

 