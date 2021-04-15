---
title: Поведение при изменении пароля единого входа
description: Предоставляет пошаговый подход к разрешению изменения пароля единого входа.
ms.assetid: c52ffeb8-ecee-4398-a7df-388b523c737c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005fe5191b3bdccf2bb1643be50817a3b0405336
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "105661673"
---
# <a name="sso-password-change-behavior"></a><span data-ttu-id="ba3cc-103">Поведение при изменении пароля единого входа</span><span class="sxs-lookup"><span data-stu-id="ba3cc-103">SSO Password Change Behavior</span></span>

<span data-ttu-id="ba3cc-104">В этом разделе приводится пошаговый подход к разрешению изменения пароля единого входа.</span><span class="sxs-lookup"><span data-stu-id="ba3cc-104">This topic provides a step-by-step approach for resolving SSO password change behavior.</span></span>

## <a name="step-by-step-approach"></a><span data-ttu-id="ba3cc-105">Пошаговый подход</span><span class="sxs-lookup"><span data-stu-id="ba3cc-105">Step-By-Step Approach</span></span>

<span data-ttu-id="ba3cc-106">В следующем списке представлен пошаговый подход к разрешению изменения пароля единого входа.</span><span class="sxs-lookup"><span data-stu-id="ba3cc-106">The following list represents a step-by-step approach for resolving SSO password change behavior.</span></span>

-   <span data-ttu-id="ba3cc-107">Когда метод EAP получает уведомление об изменении пароля, метод уведомляет EAPHost; В свою очередь, EAPHost уведомляет о обращении, возвращая код действия [еафостпирреспонсеинвокеуи](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span><span class="sxs-lookup"><span data-stu-id="ba3cc-107">Once the EAP method is notified about a password change, the method notifies EAPHost; EAPHost in turn notifies the supplicant by returning the action code, [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span></span>
-   <span data-ttu-id="ba3cc-108">После получения кода действия [еафостпирреспонсеинвокеуи](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) из EAPHost запрашивающий объект получает контекст пользовательского интерфейса от метода EAP, вызывая функцию [**еафостпиржетуиконтекст**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) . Затем EAPHost получает контекст пользовательского интерфейса из метода EAP, вызывая соответствующую функцию метода.</span><span class="sxs-lookup"><span data-stu-id="ba3cc-108">After receiving the [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) action code from EAPHost, the supplicant obtains the UI context from the EAP method by calling the [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) function; EAPHost then obtains the UI context from the EAP method by calling the corresponding method function</span></span>
-   <span data-ttu-id="ba3cc-109">Этот объект передает контекст ПОЛЬЗОВАТЕЛЬСКОГО интерфейса в процесс пользовательского интерфейса (используя некоторую форму межпроцессного взаимодействия).</span><span class="sxs-lookup"><span data-stu-id="ba3cc-109">The supplicant passes the UI context to the UI process (using some form of inter-process communication).</span></span>
-   <span data-ttu-id="ba3cc-110">Процесс пользовательского интерфейса вызывает [**еафостпиркуеринтерактивеуиинпутфиелдс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) для EAPHost.</span><span class="sxs-lookup"><span data-stu-id="ba3cc-110">The UI process calls [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) on EAPHost.</span></span>
-   <span data-ttu-id="ba3cc-111">EAPHost собирает контекст пользовательского интерфейса, вызывая [**еаппиркуеринтерактивеуиинпутфиелдс**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) для метода EAP.</span><span class="sxs-lookup"><span data-stu-id="ba3cc-111">EAPHost collects the UI context by calling [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) on the EAP method.</span></span>
-   <span data-ttu-id="ba3cc-112">Метод EAP предоставляет все необходимые сведения о контексте пользовательского интерфейса в [**структуре \_ \_ \_ данных интерактивного пользовательского интерфейса EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , где *Двдататипе* имеет значение *Еапкредекспирирек* , а *пбуидата* указывает на структуру типа [**EAP \_ cred \_ req**](eap-cred-req.md).</span><span class="sxs-lookup"><span data-stu-id="ba3cc-112">The EAP method provides any necessary UI context information in the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure, where *dwDataType* is set to *EapCredExpiryReq* and *pbUiData* points to a structure of type [**EAP\_CRED\_REQ**](eap-cred-req.md).</span></span>
-   <span data-ttu-id="ba3cc-113">При заполнении структуры [**\_ \_ \_ данных интерактивного пользовательского интерфейса EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) этот метод EAP заполнит только параметр *куркредс* и не установит флаг " [**\_ \_ PROPS" поля ввода пользовательского интерфейса EAP \_ \_ \_ \_ только для чтения**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) в структуре **\_ \_ \_ \_ данных поля ввода EAP config** .</span><span class="sxs-lookup"><span data-stu-id="ba3cc-113">While populating the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure, this EAP method will only fill in the *curCreds* parameter, and not set the [**EAP\_UI\_INPUT\_FIELD\_PROPS\_READ\_ONLY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) flag in the **EAP\_CONFIG\_INPUT\_FIELD\_DATA** structure.</span></span>
    > [!Note]  
    > <span data-ttu-id="ba3cc-114">Флаг "Свойства" [**\_ поля ввода пользовательского интерфейса EAP предназначен \_ \_ \_ \_ \_ только для чтения**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) . это поля элементов, которые необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="ba3cc-114">The [**EAP\_UI\_INPUT\_FIELD\_PROPS\_READ\_ONLY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) flag is for member field(s) which need to be changed.</span></span>

     

-   <span data-ttu-id="ba3cc-115">Собрав контекст пользовательского интерфейса сведения, процесс пользовательского интерфейса отображает пользовательский интерфейс для сбора сведений об изменении пароля от пользователя.</span><span class="sxs-lookup"><span data-stu-id="ba3cc-115">Having collected the UI context informtion, the UI process renders a UI to collect change password information from the user.</span></span> <span data-ttu-id="ba3cc-116">Эти сведения заполняются в параметре *невкредс* структуры [**требований к \_ \_ истечению \_ срока действия EAP-CRED**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req) .</span><span class="sxs-lookup"><span data-stu-id="ba3cc-116">This information is populated in the *NewCreds* parameter of the [**EAP\_CRED\_EXPIRY\_REQ**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req) structure.</span></span>
-   <span data-ttu-id="ba3cc-117">Процесс пользовательского интерфейса передает структуру [**\_ \_ ОТВ**](eap-cred-resp.md) для действия EAP обратно в EAPHost через [**еафостпиркуерюиблобфроминтерактивеуиинпутфиелдс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields).</span><span class="sxs-lookup"><span data-stu-id="ba3cc-117">The UI process passes the [**EAP\_CRED\_RESP**](eap-cred-resp.md) structure back to EAPHost via [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields).</span></span>
-   <span data-ttu-id="ba3cc-118">Процесс пользовательского интерфейса передает этот пользовательский большой двоичный объект объекту-отправитель, и он будет продолжать использовать функции времени выполнения EAPHost как обычно.</span><span class="sxs-lookup"><span data-stu-id="ba3cc-118">The UI process passes this user BLOB to the supplicant, and the supplicant continues with EAPHost run-time functions as usual.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba3cc-119">См. также</span><span class="sxs-lookup"><span data-stu-id="ba3cc-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba3cc-120">Сценарии для единого входа EAPHost</span><span class="sxs-lookup"><span data-stu-id="ba3cc-120">SSO EAPHost Scenarios</span></span>](why-eaphost-sso.md)
</dt> <dt>

[<span data-ttu-id="ba3cc-121">Единый вход и PLAP</span><span class="sxs-lookup"><span data-stu-id="ba3cc-121">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

 




