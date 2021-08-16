---
description: Используется с функциями CryptAcquireContext и Криптсетпровидер.
ms.assetid: 97e9a708-83b5-48b3-9d16-f7b54367dc4e
title: Имена поставщиков служб шифрования (Винкрипт. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c9b41aaeacb0b03df4b2fc0c608ae1f98e59ac0a581a395eb9904d0ec8e235
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768690"
---
# <a name="cryptographic-provider-names"></a>Имена поставщиков служб шифрования

Следующие имена [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP) определены в винкрипт. h. Эти константы используются с функциями [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) и [**криптсетпровидер**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovidera) .



| Константа/значение                                                                                                                                                                                                                                                                                          | Описание                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MS_DEF_DH_SCHANNEL_PROV"></span><span id="ms_def_dh_schannel_prov"></span><dl> <dt>**МС \_ DEF \_ DH \_ SChannel \_ Prov**</dt> <dt>"Microsoft DH SChannel Cryptographic Provider"</dt> </dl>      | [Поставщик служб шифрования Microsoft DSS и Диффи-Хелмана/SChannel](microsoft-dss-and-diffie-hellman-schannel-cryptographic-provider.md).<br/>                                         |
| <span id="MS_DEF_DSS_DH_PROV"></span><span id="ms_def_dss_dh_prov"></span><dl> <dt>**МС \_ DEF \_ DSS \_ DH \_ Prov**</dt> <dt>"Microsoft Base DSS и поставщик служб шифрования Diffie-Hellman"</dt> </dl>     | [Поставщик служб шифрования Microsoft Base DSS и Diffie-Hellman](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md).<br/>                                                 |
| <span id="MS_DEF_DSS_PROV"></span><span id="ms_def_dss_prov"></span><dl> <dt>**МС \_ DEF \_ DSS \_ Prov**</dt> <dt>"поставщик служб шифрования Microsoft Base DSS"</dt> </dl>                                  | [Поставщик служб шифрования Microsoft DSS](microsoft-dss-cryptographic-provider.md).<br/>                                                                                                 |
| <span id="MS_DEF_PROV"></span><span id="ms_def_prov"></span><dl> <dt>**МС \_ DEF \_ Prov**</dt> <dt>"базовый поставщик служб шифрования Майкрософт версии 1.0"</dt> </dl>                                              | [Базовый поставщик служб шифрования Майкрософт](microsoft-base-cryptographic-provider.md).<br/>                                                                                               |
| <span id="MS_DEF_RSA_SCHANNEL_PROV"></span><span id="ms_def_rsa_schannel_prov"></span><dl> <dt>**МС \_ DEF \_ RSA \_ SChannel \_ Prov**</dt> <dt>"Microsoft RSA SChannel Cryptographic Provider"</dt> </dl>  | [Поставщик служб шифрования Microsoft RSA/SChannel](microsoft-rsa-schannel-cryptographic-provider.md).<br/>                                                                               |
| <span id="MS_DEF_RSA_SIG_PROV"></span><span id="ms_def_rsa_sig_prov"></span><dl> <dt>**МС \_ DEF \_ RSA \_ SIG \_ Prov**</dt> <dt>"поставщик криптографии для подписи RSA (Майкрософт)"</dt> </dl>                | [Поставщик шифрования RSA-подписи (Майкрософт](microsoft-rsa-signature-cryptographic-provider.md) ) не поддерживается.<br/>                                                            |
| <span id="MS_ENH_DSS_DH_PROV"></span><span id="ms_enh_dss_dh_prov"></span><dl> <dt>**МС \_ ЕНХ \_ DSS \_ DH \_ Prov**</dt> <dt>"Microsoft Enhanced DSS и поставщик служб шифрования Diffie-Hellman"</dt> </dl> | [Улучшенный поставщик служб шифрования DSS и Diffie-Hellman Майкрософт](microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider.md).<br/>                                         |
| <span id="MS_ENH_RSA_AES_PROV"></span><span id="ms_enh_rsa_aes_prov"></span><dl> <dt>**МС \_ ЕНХ \_ RSA \_ AES \_ Prov**</dt> <dt>"Microsoft Enhanced RSA and AES криптографическое Provider"</dt> </dl>         | [Поставщик служб шифрования Microsoft AES](microsoft-aes-cryptographic-provider.md).<br/> * * Windows XP: * * "Microsoft Enhanced RSA and AES криптографическое Provider (Prototype)"<br/> |
| <span id="MS_ENHANCED_PROV"></span><span id="ms_enhanced_prov"></span><dl> <dt>**МС \_ УЛУЧШЕНная \_ Prov**</dt> <dt>"Microsoft Улучшенный поставщик служб шифрования версии 1.0"</dt> </dl>                           | [Расширенный поставщик служб шифрования Майкрософт](microsoft-enhanced-cryptographic-provider.md).<br/>                                                                                       |
| <span id="MS_SCARD_PROV"></span><span id="ms_scard_prov"></span><dl> <dt>**МС \_ БРОСИТЬ \_ Prov**</dt> <dt>"базовый поставщик криптографии смарт-карт Майкрософт"</dt> </dl>                                         | [Поставщик службы криптографии Microsoft Base смарт-карты](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider).<br/>                                                    |
| <span id="MS_STRONG_PROV"></span><span id="ms_strong_prov"></span><dl> <dt>**МС \_ STRONG \_ Prov**</dt> <dt>"надежный поставщик служб шифрования Майкрософт"</dt> </dl>                                        | [Поставщик строгой криптографии (Майкрософт](microsoft-strong-cryptographic-provider.md)).<br/>                                                                                           |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Винкрипт. h</dt> </dl> |



 

 
