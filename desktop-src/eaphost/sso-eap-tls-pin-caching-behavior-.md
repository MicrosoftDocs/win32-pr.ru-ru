---
title: Поведение кэширования для единого входа EAP-TLS
description: Предоставляет пошаговый подход для разрешения возобновления сеанса и повторной проверки подлинности перемещающегося пользователя в среде SSO EAP-TLS.
ms.assetid: aeded6c9-315d-4115-9750-485f017dd8dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b7c4e3058598f98327570fbcd0347cfb84e5825
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104133354"
---
# <a name="sso-eap-tls-pin-caching-behavior"></a><span data-ttu-id="805cd-103">Поведение кэширования для единого входа EAP-TLS</span><span class="sxs-lookup"><span data-stu-id="805cd-103">SSO EAP-TLS PIN Caching Behavior</span></span>

<span data-ttu-id="805cd-104">В этом разделе содержится пошаговый подход к устранению проблем возобновления сеанса и повторной проверки подлинности перемещающегося пользователя в среде SSO EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="805cd-104">This topic provides a step-by-step approach for resolving matters of session resumption and re-authentication of a roaming user in an SSO EAP-TLS environment.</span></span>

## <a name="step-by-step-approach"></a><span data-ttu-id="805cd-105">Пошаговый подход</span><span class="sxs-lookup"><span data-stu-id="805cd-105">Step-By-Step Approach</span></span>

<span data-ttu-id="805cd-106">В следующем списке представлен пошаговый подход к устранению проблемы возобновления сеанса и повторной проверки подлинности перемещающегося пользователя в среде SSO EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="805cd-106">The following list represents a step-by-step approach for resolving matters of session resumption and re-authentication of a roaming user in an SSO EAP-TLS environment.</span></span>

-   <span data-ttu-id="805cd-107">После первой успешной проверки подлинности в среде единого входа с EAP-TLS по умолчанию каждый из них будет хранить все сведения, связанные с учетными данными пользователя.</span><span class="sxs-lookup"><span data-stu-id="805cd-107">After the first successful authentication in an SSO environment with EAP-TLS, the supplicant retains all user credential related information by default.</span></span>
    > [!Note]  
    > <span data-ttu-id="805cd-108">Несмотря на то, что в соответствии с конкретной реализацией запрашивающей стороной, рекомендуется хранить всю [**структуру \_ \_ массива входных \_ полей в конфигурации EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) , которая последний раз использовался в вызове [**еафостпиркуерюсерблобфромкредентиалинпутфиелдс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) в EAPHost.</span><span class="sxs-lookup"><span data-stu-id="805cd-108">Although subject to the particular supplicant implementation, it's advisable for the supplicant to retain the entire [**EAP\_CONFIG\_INPUT\_FIELD ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure that the supplicant last used in the [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) call to EAPHost.</span></span>

     

-   <span data-ttu-id="805cd-109">При первом перемещении пользователя и запуске повторной проверки подлинности запрашивающий объект вызывает [**еафостпиркуерюсерблобфромкредентиалинпутфиелдс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) еще раз с той же структурой [**\_ \_ массива входных \_ полей EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) . Кроме того, он должен передать тот же большой двоичный объект пользователя, который сохранился после первой успешной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="805cd-109">As the user first roams and the re-authentication begins, the supplicant calls [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) again with the same [**EAP\_CONFIG\_INPUT\_FIELD ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure; the supplicant must also pass in the same user BLOB retained after the first successful authentication.</span></span>
-   <span data-ttu-id="805cd-110">Затем EAPHost передает данные из большого двоичного объекта пользователя в метод EAP.</span><span class="sxs-lookup"><span data-stu-id="805cd-110">EAPHost then passes the information in the user BLOB to the EAP method.</span></span>
-   <span data-ttu-id="805cd-111">Метод EAP, в свою очередь, обновляет BLOB-объект пользователя с полями учетных данных — ПИН-код для примера, указанный в *пеапконфигинпутфиелдаррай*, и сохраняет оставшиеся значения — например, сертификат сервера, как в исходном двоичном объекте пользователя.</span><span class="sxs-lookup"><span data-stu-id="805cd-111">The EAP method in turn updates the user BLOB with credential fields - the PIN for example - provided in *pEapConfigInputFieldArray*, and keeps the remaining values - the server certificate for example - as it was in the original user BLOB.</span></span>
-   <span data-ttu-id="805cd-112">После выполнения этих действий запрашивающий объект может возобновить проверку подлинности обычным образом, вызвав функцию времени выполнения [**еафостпирбегинсессион**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) с этим пользовательским BLOB-объектом.</span><span class="sxs-lookup"><span data-stu-id="805cd-112">After completing these steps, the supplicant can resume authentication in a normal way by calling the [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) run-time function with this user BLOB.</span></span>

## <a name="related-topics"></a><span data-ttu-id="805cd-113">См. также</span><span class="sxs-lookup"><span data-stu-id="805cd-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="805cd-114">Сценарии для единого входа EAPHost</span><span class="sxs-lookup"><span data-stu-id="805cd-114">SSO EAPHost Scenarios</span></span>](why-eaphost-sso.md)
</dt> <dt>

[<span data-ttu-id="805cd-115">Единый вход и PLAP</span><span class="sxs-lookup"><span data-stu-id="805cd-115">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

 




