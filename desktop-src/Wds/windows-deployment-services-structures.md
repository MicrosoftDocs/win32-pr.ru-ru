---
title: Структуры служб развертывания Windows
description: В службах развертывания Windows используются следующие структуры.
ms.assetid: 2e52a6ae-cecb-45de-b777-108836ed5264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20f5b369a2bbb5d68bd77dce1751e09fed2e6b6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068472"
---
# <a name="windows-deployment-services-structures"></a>Структуры служб развертывания Windows

В службах развертывания Windows используются следующие структуры.



| Структура                                                                         | Описание                                                                                                        |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**PXE- \_ адрес**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address)                                               | Указывает сетевой адрес пакета.                                                                        |
| [**\_сообщение DHCP \_ PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_message)                                    | Эта структура используется с API-сервером PXE служб развертывания Windows.                                        |
| [**\_параметр PXE DHCP \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_option)                                      | Эта структура используется с API-сервером PXE служб развертывания Windows.                                        |
| [**\_поставщик PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider)                                             | Описывает поставщик.                                                                                              |
| [**\_cred CLI \_ WDS**](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred)                                            | Содержит учетные данные, используемые для авторизации сеанса клиента.                                                           |
| [**\_запрос WDS транспортклиент \_**](/windows/desktop/api/Wdstci/ns-wdstci-wds_transportclient_request)              | Используется функцией [**вдстранспортклиентстартсессион**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) .                     |
| [**\_сведения о сеансе транспортклиент \_**](/windows/desktop/api/Wdstci/ns-wdstci-transportclient_session_info)            | Используется функцией обратного вызова [*PFN \_ вдстранспортклиентсессионстартекс*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) . |
| [**\_ \_ параметры инициализации WDS \_ транспортпровидер**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_init_params) | Используется функцией обратного вызова [**вдстранспортпровидеринитиализе**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .            |
| [**\_Параметры ТРАНСПОРТПРОВИДЕР \_ WDS**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_settings)        | Используется функцией обратного вызова [**вдстранспортпровидеринитиализе**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .            |



 

Доступны следующие возможности, начиная с Windows 8 и Windows Server 2012.

| Структура                                          | Описание                                               |
|----------------------------------------------------|-----------------------------------------------------------|
| [**PXE \_ , \_ параметр DHCPv6**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_option)   | Используется с API PXE-сервера служб развертывания Windows. |
| [**\_Сообщение DHCPv6 \_ PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_message) | Сообщение DHCPV6.                                         |



 

 

 




