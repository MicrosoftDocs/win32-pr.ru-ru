---
title: Настройка безопасности Process-Wide с помощью CoInitializeSecurity
description: Функция CoInitializeSecurity позволяет управлять сложными сценариями безопасности, устанавливая параметры безопасности приложения программным способом.
ms.assetid: 20b66868-fb9a-489f-97a2-59a8a825c8d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c3e601897e9f2313682a3474c1760bc211285d8fa81a82f67d114681a7a57f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610894"
---
# <a name="setting-process-wide-security-with-coinitializesecurity"></a>Настройка безопасности Process-Wide с помощью CoInitializeSecurity

Функция [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) позволяет управлять сложными сценариями безопасности, устанавливая параметры безопасности приложения программным способом. В этом разделе описываются сценарии использования **CoInitializeSecurity** и приводятся некоторые сведения об их использовании.

Существует несколько причин, по которым может потребоваться использовать [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) для установки безопасности на уровне процесса в рамках программы. Например, можно задать уровень проверки подлинности и разрешения на доступ к приложению с помощью dcomcnfg.exe. уровень олицетворения по умолчанию для компьютера может быть не тем, который вы хотите использовать для процесса. Единственный способ изменить этот параметр для процесса — вызвать **CoInitializeSecurity**.

Если вы хотите использовать поставщик безопасности SChannel, необходимо указать его в качестве службы проверки подлинности в вызове [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

Другой распространенный сценарий, в котором безопасность на уровне процесса можно установить программно, — когда необходимо установить безопасность по умолчанию для всего процесса, но имеется один или несколько объектов в этом процессе, которые предоставляют интерфейсы с особыми требованиями к безопасности. В этом случае можно вызвать [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) , чтобы настроить безопасность для процесса, позволяя COM обрабатывать большинство проверок безопасности, а также вызывать другие методы для настройки безопасности объектов с особыми требованиями к безопасности. Вызов этих методов и функций описывается в разделе [Настройка безопасности на уровне прокси-сервера интерфейса](setting-security-at-the-interface-proxy-level.md).

Если приложение имеет очень специализированные требования к безопасности, такие как предоставление определенным группам доступа к различным объектам в зависимости от времени суток, может потребоваться программно управлять всей безопасностью, гарантируя, что COM не будет выполнять автоматическую проверку. Для этого необходимо вызвать [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), присвоив параметру *двауснлевел* значение None, а параметр *pVoid* — **значение NULL**. При наличии собственного пакета безопасности его также необходимо зарегистрировать в параметре *пауснсвк* . Затем вы можете управлять всеми собственными средствами безопасности с помощью вызовов интерфейса уровня прокси-сервера и функций, описанных в разделе [Настройка безопасности на уровне прокси интерфейса](setting-security-at-the-interface-proxy-level.md).

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) предлагает широкий набор возможностей. При вызове **CoInitializeSecurity** значения реестра игнорируются, а вместо них используются значения инициализации безопасности, передаваемые в вызов. В зависимости от нужного результата первый параметр, *pVoid*, может указывать на три различных типа значений: [**\_ дескриптор безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , объект [**иакцессконтрол**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) или указатель на AppID. в большинстве случаев для создания **\_ дескриптора безопасности** , который будет указывать *pVoid* , будут использоваться функции Windows.

Однако *pVoid* также может указывать на объект [**иакцессконтрол**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) .

Чтобы указать [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) , что объект [**иакцессконтрол**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) передается *pVoid*, необходимо передать \_ значение управления доступом еоак в \_ параметр *двкапабилитиес* . Так как **CoInitializeSecurity** кэширует результаты проверок доступа, список управления доступом не должен изменяться после вызова **CoInitializeSecurity**.

Другой тип значения, который можно передать в параметр *pVoid* , — это указатель на идентификатор GUID, который является идентификатором приложения. Если *pVoid* является указателем на AppID, необходимо указать еоак \_ AppID в параметре *пкапабилитиес* , чтобы функция знала, какое значение должно быть в *pVoid*. Если *pVoid* указывает на AppID, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) использует только реестр для значений проверки подлинности и игнорирует все остальные параметры до **CoInitializeSecurity**.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Настройка безопасности Process-Wide](setting-processwide-security.md)
</dt> </dl>

 

 