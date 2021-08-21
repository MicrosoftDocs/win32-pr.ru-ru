---
title: Структуры IKE/AuthIP
description: Структуры IKE/AuthIP
ms.assetid: 3267EA3C-FD1F-4ED1-9794-92551222EFE1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de46cd72ec382dd360e6311930e946da3bf4189855adeaa49915b15ce3a9865
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069094"
---
# <a name="ikeauthip-structures"></a>Структуры IKE/AuthIP

## <a name="in-this-section"></a>Содержание раздела

-   [**\_METHOD0 проверки подлинности IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method0)
-   [**\_METHOD1 проверки подлинности IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method1)
-   [**\_METHOD2 проверки подлинности IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [**\_EKUS0 сертификата \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**\_NAME0 сертификата \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**\_ \_ Корневой CONFIG0 сертификата IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cert_root_config0)
-   [**\_AUTHENTICATION0 сертификата \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication0)
-   [**\_AUTHENTICATION1 сертификата \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication1)
-   [**\_Добавьте сертификата \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [**\_CREDENTIAL0 сертификата \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential0)
-   [**\_Учетные данные1 сертификата \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential1)
-   [**\_CRITERIA0 сертификата \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**\_ALGORITHM0 шифра IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cipher_algorithm0)
-   [**\_Общие \_ STATISTICS0и IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics0)
-   [**\_Общие \_ STATISTICS1и IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics1)
-   [**\_PAIR0 cookie \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cookie_pair0)
-   [**\_CREDENTIAL0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential0)
-   [**\_УЧЕТНЫЕ ДАННЫЕ1 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential1)
-   [**\_УЧЕТНЫЕ ДАННЫЕ2 IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential2)
-   [**\_CREDENTIALS0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials0)
-   [**\_CREDENTIALS1 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials1)
-   [**\_CREDENTIALS2 IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credentials2)
-   [**\_PAIR0 учетных данных для IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair0)
-   [**\_PAIR1 учетных данных для IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair1)
-   [**\_PAIR2 учетных данных для IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential_pair2)
-   [**\_AUTHENTICATION0 EAP для IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_eap_authentication0)
-   [**\_POLICY0 EM для IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy0)
-   [**\_POLICY1 EM для IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy1)
-   [**\_POLICY2 EM для IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [**\_ALGORITHM0 целостность IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_integrity_algorithm0)
-   [**\_ \_ \_ Конкретные \_ Общие \_ STATISTICS0 для IP-версии IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0)
-   [**\_ \_ \_ Конкретные \_ Общие \_ STATISTICS1 для IP-версии IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics1)
-   [**\_IP- \_ версия IKEEXT для \_ конкретного \_ кэймодуле \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics0)
-   [**\_IP- \_ версия IKEEXT для \_ конкретного \_ кэймодуле \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1)
-   [**IKEEXT \_ IPv6 \_ КГА \_ AUTHENTICATION0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0)
-   [**IKEEXT \_ Kerberos \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication0)
-   [**IKEEXT \_ Kerberos \_ AUTHENTICATION1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [**IKEEXT \_ кэймодуле \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics0)
-   [**IKEEXT \_ кэймодуле \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics1)
-   [**\_Имя IKEEXT \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_name_credential0)
-   [**\_ \_ \_ AUTHENTICATION0а NTLM v2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_ntlm_v2_authentication0)
-   [**\_POLICY0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy0)
-   [**\_POLICY1 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy1)
-   [**\_POLICY2 IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [**\_AUTHENTICATION0 с общим \_ ключом \_ для IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0)
-   [**\_AUTHENTICATION1 с общим \_ ключом \_ для IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1)
-   [**\_PROPOSAL0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_proposal0)
-   [**\_Зарезервированные \_ AUTHENTICATION0ные IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_reserved_authentication0)
-   [**\_DETAILS0 SA \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details0)
-   [**\_DETAILS1 SA \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details1)
-   [**\_DETAILS2 SA \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_sa_details2)
-   [**\_ \_ TEMPLATE0 перечисления SA для IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_enum_template0)
-   [**\_STATISTICS0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics0)
-   [**\_STATISTICS1 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics1)
-   [**\_TRAFFIC0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_traffic0)

 

 




