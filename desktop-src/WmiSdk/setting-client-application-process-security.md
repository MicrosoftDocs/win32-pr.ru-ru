---
description: Клиентские приложения, вызывающие интерфейсы WMI, могут управлять уровнями безопасности своих процессов.
ms.assetid: 790b4e40-9b92-464a-a774-dec0b75cedee
ms.tgt_platform: multiple
title: Настройка безопасности процесса клиентского приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be6b3f6e632ade53700bbe81afc7698a06fe2ff038e0c57c1b4a7eed44afa68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739478"
---
# <a name="setting-client-application-process-security"></a>Настройка безопасности процесса клиентского приложения

Клиентские приложения, вызывающие интерфейсы WMI, могут управлять уровнями безопасности своих процессов. Все приложения WMI обращаются к WMI через COM, и вы можете вызвать функцию COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) , чтобы настроить безопасность для процессов. Приложения, которые выполняют асинхронные вызовы к WMI и приложениям, зарегистрированным в качестве потребителей событий, устанавливают уровни безопасности для вызова в WMI.

Если не выполнить явный вызов [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), COM вызывает его неявно с использованием значений из реестра. Однако значения в реестре могут иметь более низкие параметры для олицетворения и проверки подлинности, которые не обеспечивают безопасность, необходимую для инструментария WMI. Дополнительные сведения см. [в разделе Задание уровня безопасности процесса по умолчанию с помощью C++](setting-the-default-process-security-level-using-c-.md).

Асинхронный доступ к инструментарию WMI не рекомендуется. Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник. Это создает угрозы безопасности для сценариев и приложений. Чтобы устранить риски, используйте семисинчронаус или синхронное взаимодействие или выполните соответствующие проверки доступа в клиентском приложении. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

При вызове любого из WMI-прокси ([**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), [**иенумвбемклассобжект**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject),[**ивбемкаллресулт**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)или [**ивбемрефрешер**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)) используется необработанный указатель. Дополнительные сведения о значениях по умолчанию и рекомендациях см. в разделе [Настройка параметров безопасности для IWbemServices и других учетных записей-посредников](setting-the-security-on-iwbemservices-and-other-proxies.md).

Следующая процедура описывает шаги, которые необходимо выполнить, чтобы настроить безопасность для WMI в процессе приложения.

**Настройка безопасности для WMI в процессе приложения**

1.  определите уровни безопасности, необходимые для операционных систем Windows, на которых выполняется клиентское приложение.
2.  Вызовите функцию COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) , чтобы задать параметры безопасности по умолчанию для процесса, в котором выполняется клиентское приложение. Здесь объявляется, какой объем безопасности требуется для доступа к процессу, в котором выполняется приложение.
3.  Если необходимо изменить безопасность на отдельном прокси-сервере, например в другом вызове [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), вызовите метод [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).
4.  Если необходимо управлять удаленным оборудованием или системным объектом, которым требуются дополнительные привилегии, используйте функцию [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) , чтобы включить необходимые привилегии. Обратите внимание, что нельзя включить привилегию, которой не назначен процесс. Дополнительные сведения см. [в разделе Проверка доступа к частным объектам](/windows/desktop/SecAuthZ/checking-access-to-private-objects).

Дополнительные сведения о настройке уровня безопасности процесса по умолчанию см. в разделе [Настройка уровня безопасности процесса по умолчанию с помощью C++](setting-the-default-process-security-level-using-c-.md) и [Задание уровня безопасности процесса по умолчанию с помощью VBScript](setting-the-default-process-security-level-using-vbscript.md).

 

 
