---
description: Указывает, может ли любой пользователь создать профиль для всех пользователей.
ms.assetid: b9bdfe85-b9d5-4dcc-a7f8-05cce9702ec3
title: Алловеверйонетокреатеаллусерпрофилес (Глобалфлагс), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowEveryoneToCreateAllUserProfiles
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 63bc4c76ccecd8c7f774dc0e73621ef3f9b19877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541047"
---
# <a name="alloweveryonetocreatealluserprofiles-globalflags-element"></a><span data-ttu-id="e4e1f-103">Алловеверйонетокреатеаллусерпрофилес (Глобалфлагс), элемент</span><span class="sxs-lookup"><span data-stu-id="e4e1f-103">allowEveryoneToCreateAllUserProfiles (globalFlags) Element</span></span>

<span data-ttu-id="e4e1f-104">Элемент **алловеверйонетокреатеаллусерпрофилес** (глобалфлагс) указывает, может ли любой пользователь создать профиль для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="e4e1f-104">The **allowEveryoneToCreateAllUserProfiles** (globalFlags) element specifies whether any user can create an all-user profile.</span></span> <span data-ttu-id="e4e1f-105">Любой пользователь компьютера может использовать профиль с любым пользователем для подключения к беспроводной сети, связанной с профилем.</span><span class="sxs-lookup"><span data-stu-id="e4e1f-105">An all-user profile can be used by any user on the machine to connect to the wireless network associated with the profile.</span></span>

<span data-ttu-id="e4e1f-106">Если **алловеверйонетокреатеаллусерпрофилес** имеет значение true, то любой пользователь может создать профиль "все пользователи".</span><span class="sxs-lookup"><span data-stu-id="e4e1f-106">If **allowEveryoneToCreateAllUserProfiles** is TRUE, than any user can create an all-user profile.</span></span> <span data-ttu-id="e4e1f-107">Если **алловеверйонетокреатеаллусерпрофилес** имеет значение false, то не все пользователи могут создать профиль для всех пользователей, а также список DACL, связанный с \_ защищенным WLAN " \_ Добавить \_ новый \_ все \_ Профили пользователей" \_ , который указывает пользователей или группы пользователей с разрешением на создание профилей всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="e4e1f-107">If **allowEveryoneToCreateAllUserProfiles** is FALSE, then not all users can create an all-user profile, and there is a DACL associated with the wlan\_secure\_add\_new\_all\_user\_profiles security object that specifies the users or user groups with permission to create all-user profiles.</span></span> <span data-ttu-id="e4e1f-108">Список DACL по умолчанию указывает, что только пользователи, вошедшие в систему в качестве члена группы "Администраторы", могут создать профиль "все пользователя".</span><span class="sxs-lookup"><span data-stu-id="e4e1f-108">The default DACL specifies that only users that are logged on as a member of the Administrators group can create an all-user profile.</span></span> <span data-ttu-id="e4e1f-109">Параметры безопасности по умолчанию можно изменить, вызвав [**влансетсекуритисеттингс**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings).</span><span class="sxs-lookup"><span data-stu-id="e4e1f-109">The default security settings can be changed by calling [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings).</span></span> <span data-ttu-id="e4e1f-110">Чтобы получить текущие параметры безопасности, вызовите [**вланжетсекуритисеттингс**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span><span class="sxs-lookup"><span data-stu-id="e4e1f-110">To get the current security settings, call [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span></span>

<span data-ttu-id="e4e1f-111">Этот элемент является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e4e1f-111">This element is mandatory.</span></span> <span data-ttu-id="e4e1f-112">При создании профиля службой автонастройки этот элемент будет иметь значение по умолчанию TRUE.</span><span class="sxs-lookup"><span data-stu-id="e4e1f-112">When a profile is created by the AutoConfig service, this element will have the default value of TRUE.</span></span>

``` syntax
<xs:element name="allowEveryoneToCreateAllUserProfiles"
    type="boolean"
 />
```

<span data-ttu-id="e4e1f-113">Элемент **алловеверйонетокреатеаллусерпрофилес** определяется элементом [**глобалфлагс**](wlan-policyschema-globalflags-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e4e1f-113">The **allowEveryoneToCreateAllUserProfiles** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4e1f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e4e1f-114">Requirements</span></span>



| <span data-ttu-id="e4e1f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e4e1f-115">Requirement</span></span> | <span data-ttu-id="e4e1f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e4e1f-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e4e1f-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4e1f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e4e1f-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e4e1f-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e4e1f-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4e1f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e4e1f-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e4e1f-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e4e1f-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4e1f-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="e4e1f-122">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="e4e1f-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e4e1f-123">**глобалфлагс**</span><span class="sxs-lookup"><span data-stu-id="e4e1f-123">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="e4e1f-124">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="e4e1f-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e4e1f-125">**Глобалфлагс (Вланполици)**</span><span class="sxs-lookup"><span data-stu-id="e4e1f-125">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




