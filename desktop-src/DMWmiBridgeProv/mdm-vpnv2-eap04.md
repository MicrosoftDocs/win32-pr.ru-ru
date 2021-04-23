---
title: Класс MDM_VPNv2_Eap04
description: Класс MDM \_ Поддержка vpnv2 \_ Eap04 содержит требуемые сведения о конфигурации XML, если в собственном профиле указана проверка подлинности EAP.
ms.assetid: 87a78743-1ee6-4b86-bfbf-62ba9059535a
keywords:
- Класс MDM_VPNv2_Eap04
- MDM_VPNv2_Eap04 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_Eap04
- MDM_VPNv2_Eap04.InstanceID
- MDM_VPNv2_Eap04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9270bf1cae37c345fe81be674e9d9afc2c533bc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803521"
---
# <a name="mdm_vpnv2_eap04-class"></a><span data-ttu-id="cdec2-105">\_Класс MDM поддержка vpnv2 \_ Eap04</span><span class="sxs-lookup"><span data-stu-id="cdec2-105">MDM\_VPNv2\_Eap04 class</span></span>

<span data-ttu-id="cdec2-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="cdec2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cdec2-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="cdec2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cdec2-108">Класс **MDM \_ Поддержка vpnv2 \_ Eap04** содержит требуемые сведения о конфигурации XML, если в собственном профиле указана проверка подлинности EAP.</span><span class="sxs-lookup"><span data-stu-id="cdec2-108">The **MDM\_VPNv2\_Eap04** class contains the required configuration XML information when the native profile specifies EAP authentication.</span></span>

<span data-ttu-id="cdec2-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="cdec2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdec2-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cdec2-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Eap04
{
  string InstanceID;
  string ParentID;
  string Configuration;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="cdec2-111">Члены</span><span class="sxs-lookup"><span data-stu-id="cdec2-111">Members</span></span>

<span data-ttu-id="cdec2-112">Класс **MDM \_ Поддержка vpnv2 \_ Eap04** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cdec2-112">The **MDM\_VPNv2\_Eap04** class has these types of members:</span></span>

-   [<span data-ttu-id="cdec2-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="cdec2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cdec2-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="cdec2-114">Properties</span></span>

<span data-ttu-id="cdec2-115">Класс **MDM \_ Поддержка vpnv2 \_ Eap04** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cdec2-115">The **MDM\_VPNv2\_Eap04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="cdec2-116">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="cdec2-116">Configuration</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-eap-configuration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdec2-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cdec2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdec2-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cdec2-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cdec2-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cdec2-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdec2-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cdec2-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdec2-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdec2-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdec2-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cdec2-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cdec2-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="cdec2-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="cdec2-124">Для этого класса строка имеет значение "EAP".</span><span class="sxs-lookup"><span data-stu-id="cdec2-124">For this class, the string is "Eap"</span></span>

</dd> <dt>

<span data-ttu-id="cdec2-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="cdec2-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdec2-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cdec2-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdec2-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdec2-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdec2-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cdec2-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cdec2-129">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="cdec2-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="cdec2-130">Для этого класса строка имеет значение "./Vendor/MSFT/VPNv2/*имя_профиля*/нативепрофиле/аусентикатион"</span><span class="sxs-lookup"><span data-stu-id="cdec2-130">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span></span>

</dd> <dt>

[<span data-ttu-id="cdec2-131">Тип</span><span class="sxs-lookup"><span data-stu-id="cdec2-131">Type</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdec2-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="cdec2-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cdec2-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cdec2-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cdec2-134">Требования</span><span class="sxs-lookup"><span data-stu-id="cdec2-134">Requirements</span></span>



| <span data-ttu-id="cdec2-135">Требование</span><span class="sxs-lookup"><span data-stu-id="cdec2-135">Requirement</span></span> | <span data-ttu-id="cdec2-136">Значение</span><span class="sxs-lookup"><span data-stu-id="cdec2-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdec2-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cdec2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="cdec2-138">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="cdec2-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cdec2-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cdec2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="cdec2-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cdec2-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="cdec2-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cdec2-141">Namespace</span></span><br/>                | <span data-ttu-id="cdec2-142">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="cdec2-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="cdec2-143">MOF</span><span class="sxs-lookup"><span data-stu-id="cdec2-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cdec2-144"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cdec2-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cdec2-145">DLL</span><span class="sxs-lookup"><span data-stu-id="cdec2-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdec2-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdec2-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdec2-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cdec2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdec2-148">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="cdec2-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

