---
description: Содержит сведения о профиле подключения 802.1 X, который сейчас используется для проверки подлинности 802.1 X.
ms.assetid: ec494c74-bc79-445a-8889-a6f441e95ac5
title: Структура ONEX_CONNECTION_PROFILE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ONEX_CONNECTION_PROFILE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 21e02a1f09d3439c64fb8124cd0cfc8140732be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683339"
---
# <a name="onex_connection_profile-structure"></a><span data-ttu-id="e479a-103">\_ \_ Структура профиля подключения ONEX</span><span class="sxs-lookup"><span data-stu-id="e479a-103">ONEX\_CONNECTION\_PROFILE structure</span></span>

<span data-ttu-id="e479a-104">Структура **\_ \_ профиля подключения ONEX** содержит сведения о профиле подключения 802.1 x, который сейчас используется для проверки подлинности 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="e479a-104">The **ONEX\_CONNECTION\_PROFILE** structure contains information on the 802.1X connection profile currently used for 802.1X authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="e479a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e479a-105">Syntax</span></span>


```C++
typedef struct _ONEX_CONNECTION_PROFILE {
  DWORD                dwVersion;
  DWORD                dwTotalLen;
  DWORD                fOneXSupplicantFlags  :1;
  DWORD                fsupplicantMode  :1;
  DWORD                fauthMode  :1;
  DWORD                fHeldPeriod  :1;
  DWORD                fAuthPeriod  :1;
  DWORD                fStartPeriod  :1;
  DWORD                fMaxStart  :1;
  DWORD                fMaxAuthFailures  :1;
  DWORD                fNetworkAuthTimeout  :1;
  DWORD                fAllowLogonDialogs  :1;
  DWORD                fNetworkAuthWithUITimeout  :1;
  DWORD                fUserBasedVLan  :1;
  DWORD                dwOneXSupplicantFlags;
  ONEX_SUPPLICANT_MODE supplicantMode;
  ONEX_AUTH_MODE       authMode;
  DWORD                dwHeldPeriod;
  DWORD                dwAuthPeriod;
  DWORD                dwStartPeriod;
  DWORD                dwMaxStart;
  DWORD                dwMaxAuthFailures;
  DWORD                dwNetworkAuthTimeout;
  DWORD                dwNetworkAuthWithUITimeout;
  BOOL                 bAllowLogonDialogs;
  BOOL                 bUserBasedVLan;
} ONEX_CONNECTION_PROFILE, *PONEX_CONNECTION_PROFILE;
```



## <a name="members"></a><span data-ttu-id="e479a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="e479a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e479a-107">**двверсион**</span><span class="sxs-lookup"><span data-stu-id="e479a-107">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-108">Версия этой структуры **\_ \_ профиля подключения ONEX** .</span><span class="sxs-lookup"><span data-stu-id="e479a-108">The version of this **ONEX\_CONNECTION\_PROFILE** structure.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-109">**двтоталлен**</span><span class="sxs-lookup"><span data-stu-id="e479a-109">**dwTotalLen**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-110">Длина в байтах этой структуры **\_ \_ профиля подключения ONEX** .</span><span class="sxs-lookup"><span data-stu-id="e479a-110">The length, in bytes, of this **ONEX\_CONNECTION\_PROFILE** structure.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-111">**фонекссуппликантфлагс**</span><span class="sxs-lookup"><span data-stu-id="e479a-111">**fOneXSupplicantFlags**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-112">Указывает, содержит ли структура **\_ \_ профиля подключения ONEX** допустимые данные в элементе **двонекссуппликантфлагс** .</span><span class="sxs-lookup"><span data-stu-id="e479a-112">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwOneXSupplicantFlags** member.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-113">**фсуппликантмоде**</span><span class="sxs-lookup"><span data-stu-id="e479a-113">**fsupplicantMode**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-114">Указывает, содержит ли структура **\_ \_ профиля подключения ONEX** допустимые данные в элементе **суппликантмоде** .</span><span class="sxs-lookup"><span data-stu-id="e479a-114">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **supplicantMode** member.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-115">**фаусмоде**</span><span class="sxs-lookup"><span data-stu-id="e479a-115">**fauthMode**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-116">Указывает, содержит ли структура **\_ \_ профиля подключения ONEX** допустимые данные в элементе **аусмоде** .</span><span class="sxs-lookup"><span data-stu-id="e479a-116">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **authMode** member.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-117">**фхелдпериод**</span><span class="sxs-lookup"><span data-stu-id="e479a-117">**fHeldPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-118">Указывает, содержит ли структура **\_ \_ профиля подключения ONEX** допустимые данные в элементе **двхелдпериод** .</span><span class="sxs-lookup"><span data-stu-id="e479a-118">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwHeldPeriod** member.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-119">**фауспериод**</span><span class="sxs-lookup"><span data-stu-id="e479a-119">**fAuthPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-120">Указывает, содержит ли структура **\_ \_ профиля подключения ONEX** допустимые данные в элементе **двауспериод** .</span><span class="sxs-lookup"><span data-stu-id="e479a-120">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwAuthPeriod** member.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-121">**фстартпериод**</span><span class="sxs-lookup"><span data-stu-id="e479a-121">**fStartPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-122">Указывает, содержит ли структура **\_ \_ профиля подключения ONEX** допустимые данные в элементе **двстартпериод** .</span><span class="sxs-lookup"><span data-stu-id="e479a-122">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwStartPeriod** member.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-123">**фмаксстарт**</span><span class="sxs-lookup"><span data-stu-id="e479a-123">**fMaxStart**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-124">Указывает, содержит ли структура **\_ \_ профиля подключения ONEX** допустимые данные в элементе **двмаксстарт** .</span><span class="sxs-lookup"><span data-stu-id="e479a-124">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwMaxStart** member.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-125">**фмаксаусфаилурес**</span><span class="sxs-lookup"><span data-stu-id="e479a-125">**fMaxAuthFailures**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-126">Указывает, содержит ли структура **\_ \_ профиля подключения ONEX** допустимые данные в элементе **двмаксаусфаилурес** .</span><span class="sxs-lookup"><span data-stu-id="e479a-126">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwMaxAuthFailures** member.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-127">**фнетворкаустимеаут**</span><span class="sxs-lookup"><span data-stu-id="e479a-127">**fNetworkAuthTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-128">Указывает, содержит ли структура **\_ \_ профиля подключения ONEX** допустимые данные в элементе **двнетворкаустимеаут** .</span><span class="sxs-lookup"><span data-stu-id="e479a-128">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwNetworkAuthTimeout** member.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-129">**фалловлогондиалогс**</span><span class="sxs-lookup"><span data-stu-id="e479a-129">**fAllowLogonDialogs**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-130">Указывает, содержит ли структура **\_ \_ профиля подключения ONEX** допустимые данные в элементе **балловлогондиалогс** .</span><span class="sxs-lookup"><span data-stu-id="e479a-130">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **bAllowLogonDialogs** member.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-131">**фнетворкаусвисуитимеаут**</span><span class="sxs-lookup"><span data-stu-id="e479a-131">**fNetworkAuthWithUITimeout**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-132">Указывает, содержит ли структура **\_ \_ профиля подключения ONEX** допустимые данные в элементе **двнетворкаусвисуитимеаут** .</span><span class="sxs-lookup"><span data-stu-id="e479a-132">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwNetworkAuthWithUITimeout** member.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-133">**фусербаседвлан**</span><span class="sxs-lookup"><span data-stu-id="e479a-133">**fUserBasedVLan**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-134">Указывает, содержит ли структура **\_ \_ профиля подключения ONEX** допустимые данные в элементе **бусербаседвлан** .</span><span class="sxs-lookup"><span data-stu-id="e479a-134">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **bUserBasedVLan** member.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-135">**двонекссуппликантфлагс**</span><span class="sxs-lookup"><span data-stu-id="e479a-135">**dwOneXSupplicantFlags**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-136">Набор флагов 802.1 X, которые могут присутствовать в профиле.</span><span class="sxs-lookup"><span data-stu-id="e479a-136">A set of 802.1X flags that can be present in the profile.</span></span> <span data-ttu-id="e479a-137">Эти флаги зарезервированы для внутреннего использования модулем проверки подлинности 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="e479a-137">These flags are reserved for internal use by the 802.1X authentication module.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-138">**суппликантмоде**</span><span class="sxs-lookup"><span data-stu-id="e479a-138">**supplicantMode**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-139">Элемент Суппликантмоде в схеме 802.1 X, указывающий метод передачи, используемый для EAPOL-Start сообщений.</span><span class="sxs-lookup"><span data-stu-id="e479a-139">The supplicantMode element in the 802.1X schema that specifies the method of transmission used for EAPOL-Start messages.</span></span> <span data-ttu-id="e479a-140">Дополнительные сведения см. в описании [**элемента суппликантмоде (OneX)**](onexschema-supplicantmode-onex-element.md) в схеме 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="e479a-140">For more information, see the [**supplicantMode (OneX) Element**](onexschema-supplicantmode-onex-element.md) in the 802.1X scheme.</span></span>



| <span data-ttu-id="e479a-141">Значение</span><span class="sxs-lookup"><span data-stu-id="e479a-141">Value</span></span>                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="e479a-142">Значение</span><span class="sxs-lookup"><span data-stu-id="e479a-142">Meaning</span></span>                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXSupplicantModeInhibitTransmission"></span><span id="onexsupplicantmodeinhibittransmission"></span><span id="ONEXSUPPLICANTMODEINHIBITTRANSMISSION"></span><dl> <span data-ttu-id="e479a-143"><dt>**Онекссуппликантмодеинхибиттрансмиссион**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e479a-143"><dt>**OneXSupplicantModeInhibitTransmission**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="e479a-144">EAPOL-Start сообщения не передаются.</span><span class="sxs-lookup"><span data-stu-id="e479a-144">EAPOL-Start messages are not transmitted.</span></span> <span data-ttu-id="e479a-145">Допустимо только для профилей проводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="e479a-145">Valid for wired LAN profiles only.</span></span><br/>                                                                                             |
| <span id="OneXSupplicantModeLearn"></span><span id="onexsupplicantmodelearn"></span><span id="ONEXSUPPLICANTMODELEARN"></span><dl> <span data-ttu-id="e479a-146"><dt>**Онекссуппликантмоделеарн**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e479a-146"><dt>**OneXSupplicantModeLearn**</dt> <dt>1</dt></span></span> </dl>                                                         | <span data-ttu-id="e479a-147">Клиент определяет, когда следует отсылать пакеты EAPOL-Start на основе сетевых возможностей.</span><span class="sxs-lookup"><span data-stu-id="e479a-147">The client determines when to send EAPOL-Start packets based on network capability.</span></span> <span data-ttu-id="e479a-148">EAPOL-Start сообщения отправляются только при необходимости.</span><span class="sxs-lookup"><span data-stu-id="e479a-148">EAPOL-Start messages are only sent when required.</span></span> <span data-ttu-id="e479a-149">Допустимо только для профилей проводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="e479a-149">Valid for wired LAN profiles only.</span></span><br/> |
| <span id="OneXSupplicantModeCompliant"></span><span id="onexsupplicantmodecompliant"></span><span id="ONEXSUPPLICANTMODECOMPLIANT"></span><dl> <span data-ttu-id="e479a-150"><dt>**Онекссуппликантмодекомплиант**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e479a-150"><dt>**OneXSupplicantModeCompliant**</dt> <dt>2</dt></span></span> </dl>                                         | <span data-ttu-id="e479a-151">EAPOL-Start сообщения передаются, как указано в 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="e479a-151">EAPOL-Start messages are transmitted as specified by 802.1X.</span></span> <span data-ttu-id="e479a-152">Допустимо для профилей проводной и беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="e479a-152">Valid for both wired and wireless LAN profiles.</span></span><br/>                                                             |



 

</dd> <dt>

<span data-ttu-id="e479a-153">**аусмоде**</span><span class="sxs-lookup"><span data-stu-id="e479a-153">**authMode**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-154">Элемент Аусмоде в схеме 802.1 X, указывающий тип учетных данных, используемых для проверки подлинности 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="e479a-154">The authMode element in the 802.1X schema that specifies the type of credentials used for 802.1X authentication.</span></span> <span data-ttu-id="e479a-155">Дополнительные сведения см. в описании [**элемента аусмоде (OneX)**](onexschema-authmode-onex-element.md) в схеме 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="e479a-155">For more information, see the [**authMode (OneX) Element**](onexschema-authmode-onex-element.md) in the 802.1X scheme.</span></span>



| <span data-ttu-id="e479a-156">Значение</span><span class="sxs-lookup"><span data-stu-id="e479a-156">Value</span></span>                                                                                                                                                                                                                                                                                               | <span data-ttu-id="e479a-157">Значение</span><span class="sxs-lookup"><span data-stu-id="e479a-157">Meaning</span></span>                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXAuthModeMachineOrUser"></span><span id="onexauthmodemachineoruser"></span><span id="ONEXAUTHMODEMACHINEORUSER"></span><dl> <span data-ttu-id="e479a-158"><dt>**Онексаусмодемачинеорусер**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e479a-158"><dt>**OneXAuthModeMachineOrUser**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="e479a-159">Используйте учетные данные компьютера или пользователя.</span><span class="sxs-lookup"><span data-stu-id="e479a-159">Use machine or user credentials.</span></span> <span data-ttu-id="e479a-160">При входе пользователя в систему для проверки подлинности используются учетные данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="e479a-160">When a user is logged on, the user's credentials are used for authentication.</span></span> <span data-ttu-id="e479a-161">Если пользователь не вошел в систему, используются учетные данные компьютера.</span><span class="sxs-lookup"><span data-stu-id="e479a-161">When no user is logged on, machine credentials are used.</span></span><br/> |
| <span id="OneXAuthModeMachineOnly"></span><span id="onexauthmodemachineonly"></span><span id="ONEXAUTHMODEMACHINEONLY"></span><dl> <span data-ttu-id="e479a-162"><dt>**Онексаусмодемачинеонли**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e479a-162"><dt>**OneXAuthModeMachineOnly**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="e479a-163">Использовать только учетные данные компьютера.</span><span class="sxs-lookup"><span data-stu-id="e479a-163">Use machine credentials only.</span></span><br/>                                                                                                                                           |
| <span id="OneXAuthModeUserOnly"></span><span id="onexauthmodeuseronly"></span><span id="ONEXAUTHMODEUSERONLY"></span><dl> <span data-ttu-id="e479a-164"><dt>**Онексаусмодеусеронли**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e479a-164"><dt>**OneXAuthModeUserOnly**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="e479a-165">Используйте только учетные данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="e479a-165">Use user credentials only.</span></span><br/>                                                                                                                                              |
| <span id="OneXAuthModeGuest"></span><span id="onexauthmodeguest"></span><span id="ONEXAUTHMODEGUEST"></span><dl> <span data-ttu-id="e479a-166"><dt>**Онексаусмодегуест**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e479a-166"><dt>**OneXAuthModeGuest**</dt> <dt>3</dt></span></span> </dl>                                 | <span data-ttu-id="e479a-167">Используйте только гостевые (пустые) учетные данные.</span><span class="sxs-lookup"><span data-stu-id="e479a-167">Use guest (empty) credentials only.</span></span><br/>                                                                                                                                     |
| <span id="OneXAuthModeUnspecified"></span><span id="onexauthmodeunspecified"></span><span id="ONEXAUTHMODEUNSPECIFIED"></span><dl> <span data-ttu-id="e479a-168"><dt>**ОнексаусмодеунспеЦифиед**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e479a-168"><dt>**OneXAuthModeUnspecified**</dt> <dt>4</dt></span></span> </dl>         | <span data-ttu-id="e479a-169">Не указаны учетные данные для использования.</span><span class="sxs-lookup"><span data-stu-id="e479a-169">Credentials to use are not specified.</span></span><br/>                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="e479a-170">**двхелдпериод**</span><span class="sxs-lookup"><span data-stu-id="e479a-170">**dwHeldPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-171">Элемент Хелдпериод в схеме 802.1 X, указывающий период времени в секундах, в течение которого клиент не будет повторно пытаться пройти проверку подлинности после неудачной попытки проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e479a-171">The heldPeriod element in the 802.1X schema that specifies the length of time, in seconds, in which a client will not re-attempt authentication after a failed authentication attempt.</span></span> <span data-ttu-id="e479a-172">Дополнительные сведения см. в описании [**элемента хелдпериод (OneX)**](onexschema-heldperiod-onex-element.md) в схеме 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="e479a-172">For more information, see the [**heldPeriod (OneX) Element**](onexschema-heldperiod-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-173">**двауспериод**</span><span class="sxs-lookup"><span data-stu-id="e479a-173">**dwAuthPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-174">Элемент Ауспериод в схеме 802.1 X, указывающий максимальный интервал времени (в секундах), в течение которого клиент ожидает ответа от средства проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e479a-174">The authPeriod element in the 802.1X schema that specifies the maximum length of time, in seconds, in which a client waits for a response from the authenticator.</span></span> <span data-ttu-id="e479a-175">Если ответ не получен в течение указанного периода, клиент предполагает, что в сети отсутствует средство проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e479a-175">If a response is not received within the specified period, the client assumes that there is no authenticator present on the network.</span></span> <span data-ttu-id="e479a-176">Дополнительные сведения см. в описании [**элемента ауспериод (OneX)**](onexschema-authperiod-onex-element.md) в схеме 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="e479a-176">For more information, see the [**authPeriod (OneX) Element**](onexschema-authperiod-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-177">**двстартпериод**</span><span class="sxs-lookup"><span data-stu-id="e479a-177">**dwStartPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-178">Элемент Стартпериод в схеме 802.1 X, указывающий продолжительность времени ожидания (в секундах) перед отправкой EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="e479a-178">The startPeriod element in the 802.1X schema that specifies the length of time, in seconds, to wait before an EAPOL-Start is sent.</span></span> <span data-ttu-id="e479a-179">Для запуска процесса проверки подлинности 802.1 X отправляется сообщение EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="e479a-179">An EAPOL-Start message is sent to start the 802.1X authentication process.</span></span> <span data-ttu-id="e479a-180">Дополнительные сведения см. в описании [**элемента стартпериод (OneX)**](onexschema-startperiod-onex-element.md) в схеме 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="e479a-180">For more information, see the [**startPeriod (OneX) Element**](onexschema-startperiod-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-181">**двмаксстарт**</span><span class="sxs-lookup"><span data-stu-id="e479a-181">**dwMaxStart**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-182">Элемент Максстарт в схеме 802.1 X, указывающий максимальное число отправленных сообщений EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="e479a-182">The maxStart element in the 802.1X schema that specifies the maximum number of EAPOL-Start messages sent.</span></span> <span data-ttu-id="e479a-183">После отправки максимального числа EAPOL-Start сообщений клиент предполагает, что в сети отсутствует средство проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e479a-183">After the maximum number of EAPOL-Start messages has been sent, the client assumes that there is no authenticator present on the network.</span></span> <span data-ttu-id="e479a-184">Дополнительные сведения см. в описании [**элемента максстарт (OneX)**](onexschema-maxstart-onex-element.md) в схеме 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="e479a-184">For more information, see the [**maxStart (OneX) Element**](onexschema-maxstart-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-185">**двмаксаусфаилурес**</span><span class="sxs-lookup"><span data-stu-id="e479a-185">**dwMaxAuthFailures**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-186">Элемент Максаусфаилурес в схеме 802.1 X, указывающий максимальное количество ошибок проверки подлинности, разрешенных для набора учетных данных.</span><span class="sxs-lookup"><span data-stu-id="e479a-186">The maxAuthFailures element in the 802.1X schema that specifies the maximum number of authentication failures allowed for a set of credentials.</span></span> <span data-ttu-id="e479a-187">Дополнительные сведения см. в описании элемента [**максаусфаилурес (OneX)**](onexschema-maxauthfailures-onex-element.md) в схеме 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="e479a-187">For more information, see the [**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md) element in the 802.1X schema.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-188">**двнетворкаустимеаут**</span><span class="sxs-lookup"><span data-stu-id="e479a-188">**dwNetworkAuthTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-189">Время ожидания завершения проверки подлинности 802.1 X (в секундах) перед нормальным входом в систему.</span><span class="sxs-lookup"><span data-stu-id="e479a-189">The time, in seconds, to wait for 802.1X authentication completion before normal logon proceeds.</span></span> <span data-ttu-id="e479a-190">Это значение используется в сценариях единого signon (SSO).</span><span class="sxs-lookup"><span data-stu-id="e479a-190">This value is used in single signon (SSO) scenarios.</span></span> <span data-ttu-id="e479a-191">По умолчанию это значение равно 10 секундам в профиле 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="e479a-191">This value defaults to 10 seconds in an 802.1X profile.</span></span> <span data-ttu-id="e479a-192">Дополнительные сведения см. в описании [**элемента максделай (singleSignOn)**](onexschema-maxdelay-singlesignon-element.md) в схеме 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="e479a-192">For more information, see the [**maxDelay (singleSignOn) Element**](onexschema-maxdelay-singlesignon-element.md) in the 802.1X schema.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-193">**двнетворкаусвисуитимеаут**</span><span class="sxs-lookup"><span data-stu-id="e479a-193">**dwNetworkAuthWithUITimeout**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-194">Максимальная продолжительность (в секундах) ожидания соединения в случае, если диалоговое окно пользовательского интерфейса требует ввода данных пользователем во время единого входа.</span><span class="sxs-lookup"><span data-stu-id="e479a-194">The maximum duration time, in seconds, to wait for a connection in case a user interface dialog box that requires user input is displayed during the per-logon SSO.</span></span>

<span data-ttu-id="e479a-195">В Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях это значение жестко равно 10 минутам и не может быть настроено.</span><span class="sxs-lookup"><span data-stu-id="e479a-195">On Windows Vista with SP1 and later, this value is hardcoded to 10 minutes and is not configurable.</span></span> <span data-ttu-id="e479a-196">В выпуске Windows Vista в производство это значение по умолчанию равно 60 секундам в профиле 802.1 X и управляется элементом **максделайвисаддитионалдиалогс** в схеме.</span><span class="sxs-lookup"><span data-stu-id="e479a-196">On Windows Vista Release to Manufacturing, this value defaults to 60 seconds in an 802.1X profile and was controlled by the **maxDelayWithAdditionalDialogs** element in the schema.</span></span>

<span data-ttu-id="e479a-197">В Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях элемент **максделайвисаддитионалдиалогс** в схеме 802.1 x игнорируется и не считается устаревшим.</span><span class="sxs-lookup"><span data-stu-id="e479a-197">On Windows Vista with SP1 and later, the **maxDelayWithAdditionalDialogs** element in the 802.1X schema is ignored and deprecated.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-198">**балловлогондиалогс**</span><span class="sxs-lookup"><span data-stu-id="e479a-198">**bAllowLogonDialogs**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-199">Значение типа, указывающее, разрешать ли отображение диалоговых окон EAP при использовании единого входа с предварительным входом.</span><span class="sxs-lookup"><span data-stu-id="e479a-199">A value that specifies whether to allow EAP dialogs to be displayed when using pre-logon SSO.</span></span> <span data-ttu-id="e479a-200">Дополнительные сведения см. в описании элемента **алловаддитионалдиалогс** в схеме 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="e479a-200">For more information, see the **allowAdditionalDialogs** element in the 802.1X schema.</span></span>

</dd> <dt>

<span data-ttu-id="e479a-201">**бусербаседвлан**</span><span class="sxs-lookup"><span data-stu-id="e479a-201">**bUserBasedVLan**</span></span>
</dt> <dd>

<span data-ttu-id="e479a-202">Элемент Усербаседвиртуаллан в схеме 802.1 X, указывающий, изменяется ли виртуальная локальная сеть (VLAN), используемая устройством, на основе учетных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="e479a-202">The userBasedVirtualLan element in the 802.1X schema that specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span> <span data-ttu-id="e479a-203">Некоторые устройства сервера сетевого доступа (NAS) изменяют виртуальную локальную сеть после проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="e479a-203">Some network access server (NAS) devices change the VLAN after a user authenticates.</span></span> <span data-ttu-id="e479a-204">Когда Усербаседвиртуаллан имеет значение TRUE, NAS может изменить виртуальную ЛС устройства после проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="e479a-204">When userBasedVirtualLan is TRUE, the NAS may change a device's VLAN after a user authenticates.</span></span> <span data-ttu-id="e479a-205">Дополнительные сведения см. в описании [**элемента усербаседвиртуаллан (singleSignOn)**](onexschema-userbasedvirtuallan-singlesignon-element.md) в схеме 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="e479a-205">For more information, see the [**userBasedVirtualLan (singleSignOn) Element**](onexschema-userbasedvirtuallan-singlesignon-element.md) in the 802.1X scheme.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e479a-206">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e479a-206">Remarks</span></span>

<span data-ttu-id="e479a-207">Структура **\_ \_ профиля подключения ONEX** используется модулем 802.1 x, новым компонентом настройки беспроводной связи, поддерживаемым в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="e479a-207">The **ONEX\_CONNECTION\_PROFILE** structure is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and later.</span></span>

<span data-ttu-id="e479a-208">[**\_ \_ \_ Данные обновления результатов ONEX**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) содержат сведения об изменении состояния проверки подлинности 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="e479a-208">The [**ONEX\_RESULT\_UPDATE\_DATA**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) contains information on a status change to 802.1X authentication.</span></span> <span data-ttu-id="e479a-209">Структура **\_ \_ \_ данных обновления результатов ONEX** возвращается, если элемент **нотификатионсаурце** структуры [**\_ \_ данных уведомления WLAN**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) является **\_ \_ \_ ONEX источника уведомлений WLAN** и членом **нотификатионкоде** структуры **\_ \_ данных уведомления WLAN** для получения уведомления является **онекснотификатионтипересултупдате**.</span><span class="sxs-lookup"><span data-stu-id="e479a-209">The **ONEX\_RESULT\_UPDATE\_DATA** structure is returned when the **NotificationSource** member of the [**WLAN\_NOTIFICATION\_DATA**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) structure is **WLAN\_NOTIFICATION\_SOURCE\_ONEX** and the **NotificationCode** member of the **WLAN\_NOTIFICATION\_DATA** structure for received notification is **OneXNotificationTypeResultUpdate**.</span></span> <span data-ttu-id="e479a-210">Для этого уведомления элемент **pData** структуры **\_ \_ данных уведомления WLAN** указывает на структуру **\_ \_ \_ данных обновления результатов ONEX** , содержащую сведения об изменении состояния проверки подлинности 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="e479a-210">For this notification, the **pData** member of the **WLAN\_NOTIFICATION\_DATA** structure points to an **ONEX\_RESULT\_UPDATE\_DATA** structure that contains information on the 802.1X authentication status change.</span></span>

<span data-ttu-id="e479a-211">Если задан элемент **фонексауспарамс** в структуре [**\_ \_ \_ данных обновления результатов OneX**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) , то элемент **ауспарамс** в структуре **\_ \_ \_ данных обновления результатов OneX** содержит структуру [**\_ \_ больших двоичных объектов OneX**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob) с внедренной структурой [**\_ \_ параметров проверки подлинности OneX**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params) , начиная с элемента **двоффсет** в **\_ \_ объекте переменной ONEX**.</span><span class="sxs-lookup"><span data-stu-id="e479a-211">If the **fOneXAuthParams** member in the [**ONEX\_RESULT\_UPDATE\_DATA**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) structure is set, then the **authParams** member of the **ONEX\_RESULT\_UPDATE\_DATA** structure contains an [**ONEX\_VARIABLE\_BLOB**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob) structure with an [**ONEX\_AUTH\_PARAMS**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params) structure embedded starting at the **dwOffset** member of the **ONEX\_VARIABLE\_BLOB**.</span></span> <span data-ttu-id="e479a-212">Член **онексконнпрофиле** структуры **\_ \_ параметров проверки подлинности OneX** содержит структуру **\_ \_ больших двоичных объектов OneX** с внедренной структурой **\_ \_ профиля подключения OneX** , которая начинается с элемента **двоффсет** в **\_ \_ объекте переменной ONEX**.</span><span class="sxs-lookup"><span data-stu-id="e479a-212">The **oneXConnProfile** member of the **ONEX\_AUTH\_PARAMS** structure contains an **ONEX\_VARIABLE\_BLOB** structure with an **ONEX\_CONNECTION\_PROFILE** structure embedded starting at the **dwOffset** member of the **ONEX\_VARIABLE\_BLOB**.</span></span>

<span data-ttu-id="e479a-213">Структура **\_ \_ профиля подключения ONEX** не определена в файле общедоступного заголовка.</span><span class="sxs-lookup"><span data-stu-id="e479a-213">The **ONEX\_CONNECTION\_PROFILE** structure is not defined in a public header file.</span></span>

## <a name="requirements"></a><span data-ttu-id="e479a-214">Требования</span><span class="sxs-lookup"><span data-stu-id="e479a-214">Requirements</span></span>



| <span data-ttu-id="e479a-215">Требование</span><span class="sxs-lookup"><span data-stu-id="e479a-215">Requirement</span></span> | <span data-ttu-id="e479a-216">Значение</span><span class="sxs-lookup"><span data-stu-id="e479a-216">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e479a-217">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e479a-217">Minimum supported client</span></span><br/> | <span data-ttu-id="e479a-218">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e479a-218">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e479a-219">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e479a-219">Minimum supported server</span></span><br/> | <span data-ttu-id="e479a-220">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e479a-220">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e479a-221">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e479a-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e479a-222">Сведения об архитектуре ACM</span><span class="sxs-lookup"><span data-stu-id="e479a-222">About the ACM Architecture</span></span>](about-the-acm-architecture.md)
</dt> <dt>

[<span data-ttu-id="e479a-223">Схема OneX</span><span class="sxs-lookup"><span data-stu-id="e479a-223">OneX Schema</span></span>](onexschema-schema.md)
</dt> <dt>

[<span data-ttu-id="e479a-224">**Элемент Аусмоде (OneX)**</span><span class="sxs-lookup"><span data-stu-id="e479a-224">**authMode (OneX) Element**</span></span>](onexschema-authmode-onex-element.md)
</dt> <dt>

[<span data-ttu-id="e479a-225">**Элемент Ауспериод (OneX)**</span><span class="sxs-lookup"><span data-stu-id="e479a-225">**authPeriod (OneX) Element**</span></span>](onexschema-authperiod-onex-element.md)
</dt> <dt>

[<span data-ttu-id="e479a-226">**Элемент Хелдпериод (OneX)**</span><span class="sxs-lookup"><span data-stu-id="e479a-226">**heldPeriod (OneX) Element**</span></span>](onexschema-heldperiod-onex-element.md)
</dt> <dt>

[<span data-ttu-id="e479a-227">**Максаусфаилурес (OneX)**</span><span class="sxs-lookup"><span data-stu-id="e479a-227">**maxAuthFailures (OneX)**</span></span>](onexschema-maxauthfailures-onex-element.md)
</dt> <dt>

[<span data-ttu-id="e479a-228">**Элемент Максстарт (OneX)**</span><span class="sxs-lookup"><span data-stu-id="e479a-228">**maxStart (OneX) Element**</span></span>](onexschema-maxstart-onex-element.md)
</dt> <dt>

[<span data-ttu-id="e479a-229">**Элемент Стартпериод (OneX)**</span><span class="sxs-lookup"><span data-stu-id="e479a-229">**startPeriod (OneX) Element**</span></span>](onexschema-startperiod-onex-element.md)
</dt> <dt>

[<span data-ttu-id="e479a-230">**Элемент Суппликантмоде (OneX)**</span><span class="sxs-lookup"><span data-stu-id="e479a-230">**supplicantMode (OneX) Element**</span></span>](onexschema-supplicantmode-onex-element.md)
</dt> <dt>

[<span data-ttu-id="e479a-231">**Усербаседвиртуаллан (singleSignOn), элемент**</span><span class="sxs-lookup"><span data-stu-id="e479a-231">**userBasedVirtualLan (singleSignOn) Element**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md)
</dt> <dt>

[<span data-ttu-id="e479a-232">**\_Параметры проверки подлинности ONEX \_**</span><span class="sxs-lookup"><span data-stu-id="e479a-232">**ONEX\_AUTH\_PARAMS**</span></span>](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params)
</dt> <dt>

[<span data-ttu-id="e479a-233">**\_тип уведомления \_ ONEX**</span><span class="sxs-lookup"><span data-stu-id="e479a-233">**ONEX\_NOTIFICATION\_TYPE**</span></span>](/windows/desktop/api/dot1x/ne-dot1x-onex_notification_type)
</dt> <dt>

[<span data-ttu-id="e479a-234">**\_ \_ данные обновления результатов \_ ONEX**</span><span class="sxs-lookup"><span data-stu-id="e479a-234">**ONEX\_RESULT\_UPDATE\_DATA**</span></span>](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data)
</dt> <dt>

[<span data-ttu-id="e479a-235">**Элемент схемы OneX**</span><span class="sxs-lookup"><span data-stu-id="e479a-235">**OneX Schema Element**</span></span>](onexschema-onex-element.md)
</dt> <dt>

[<span data-ttu-id="e479a-236">**\_BLOB- \_ объект переменной ONEX**</span><span class="sxs-lookup"><span data-stu-id="e479a-236">**ONEX\_VARIABLE\_BLOB**</span></span>](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob)
</dt> <dt>

<span data-ttu-id="e479a-237">[**\_данные уведомления \_ WLAN**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e479a-237">[**WLAN\_NOTIFICATION\_DATA**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e479a-238">**вланрегистернотификатион**</span><span class="sxs-lookup"><span data-stu-id="e479a-238">**WlanRegisterNotification**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
</dt> </dl>

 

 
