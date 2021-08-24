---
title: Windows Структуры служб развертывания
description: в службах Windows Deployment Services используются следующие структуры.
ms.assetid: 2e52a6ae-cecb-45de-b777-108836ed5264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4315ccd3d9540334b00f43fda6522e3eae28be2d038cfdd56fcd129e9e0aed7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760254"
---
# <a name="windows-deployment-services-structures"></a>Windows Структуры служб развертывания

в службах Windows Deployment Services используются следующие структуры.



| Структура                                                                         | Описание                                                                                                        |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**PXE- \_ адрес**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address)                                               | Указывает сетевой адрес пакета.                                                                        |
| [**\_сообщение DHCP \_ PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_message)                                    | эта структура используется с API PXE-сервера служб Windows Deployment Services.                                        |
| [**\_параметр PXE DHCP \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_option)                                      | эта структура используется с API PXE-сервера служб Windows Deployment Services.                                        |
| [**\_поставщик PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider)                                             | Описывает поставщик.                                                                                              |
| [**\_cred CLI \_ WDS**](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred)                                            | Содержит учетные данные, используемые для авторизации сеанса клиента.                                                           |
| [**\_запрос WDS транспортклиент \_**](/windows/desktop/api/Wdstci/ns-wdstci-wds_transportclient_request)              | Используется функцией [**вдстранспортклиентстартсессион**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) .                     |
| [**\_сведения о сеансе транспортклиент \_**](/windows/desktop/api/Wdstci/ns-wdstci-transportclient_session_info)            | Используется функцией обратного вызова [*PFN \_ вдстранспортклиентсессионстартекс*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) . |
| [**\_ \_ параметры инициализации WDS \_ транспортпровидер**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_init_params) | Используется функцией обратного вызова [**вдстранспортпровидеринитиализе**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .            |
| [**\_Параметры ТРАНСПОРТПРОВИДЕР \_ WDS**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_settings)        | Используется функцией обратного вызова [**вдстранспортпровидеринитиализе**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .            |



 

доступны следующие возможности, начиная с Windows 8 и Windows Server 2012.

| Структура                                          | Описание                                               |
|----------------------------------------------------|-----------------------------------------------------------|
| [**PXE \_ , \_ параметр DHCPv6**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_option)   | используется с API PXE-сервера служб Windows Deployment Services. |
| [**\_Сообщение DHCPv6 \_ PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_message) | Сообщение DHCPV6.                                         |



 

 

 




