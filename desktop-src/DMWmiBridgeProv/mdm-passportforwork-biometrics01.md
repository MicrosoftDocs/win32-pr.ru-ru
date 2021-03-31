---
title: Класс MDM_PassportForWork_Biometrics01
description: Класс MDM \_ пасспортфорворк \_ Biometrics01 определяет параметры биометрических параметров.
ms.assetid: 64012526-eac6-4f01-8665-2bd460bc1b93
keywords:
- Класс MDM_PassportForWork_Biometrics01
- MDM_PassportForWork_Biometrics01 класс, описание
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Biometrics01
- MDM_PassportForWork_Biometrics01.InstanceID
- MDM_PassportForWork_Biometrics01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 132351f17b6f242e39d6e6d6680aa756d5f7b5f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135563"
---
# <a name="mdm_passportforwork_biometrics01-class"></a><span data-ttu-id="3e6a3-105">\_Класс MDM пасспортфорворк \_ Biometrics01</span><span class="sxs-lookup"><span data-stu-id="3e6a3-105">MDM\_PassportForWork\_Biometrics01 class</span></span>

<span data-ttu-id="3e6a3-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="3e6a3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3e6a3-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="3e6a3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3e6a3-108">Класс **MDM \_ пасспортфорворк \_ Biometrics01** определяет параметры биометрических параметров.</span><span class="sxs-lookup"><span data-stu-id="3e6a3-108">The **MDM\_PassportForWork\_Biometrics01** class defines biometric settings.</span></span>

<span data-ttu-id="3e6a3-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="3e6a3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e6a3-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e6a3-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Biometrics01
{
  string  InstanceID;
  string  ParentID;
  boolean UseBiometrics;
  boolean FacialFeaturesUseEnhancedAntiSpoofing;
};
```

## <a name="members"></a><span data-ttu-id="3e6a3-111">Члены</span><span class="sxs-lookup"><span data-stu-id="3e6a3-111">Members</span></span>

<span data-ttu-id="3e6a3-112">Класс **MDM \_ пасспортфорворк \_ Biometrics01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3e6a3-112">The **MDM\_PassportForWork\_Biometrics01** class has these types of members:</span></span>

-   [<span data-ttu-id="3e6a3-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="3e6a3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e6a3-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="3e6a3-114">Properties</span></span>

<span data-ttu-id="3e6a3-115">Класс **MDM \_ пасспортфорворк \_ Biometrics01** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3e6a3-115">The **MDM\_PassportForWork\_Biometrics01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3e6a3-116">фаЦиалфеатуресусинханцедантиспуфинг</span><span class="sxs-lookup"><span data-stu-id="3e6a3-116">FacialFeaturesUseEnhancedAntiSpoofing</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e6a3-117">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3e6a3-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3e6a3-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3e6a3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3e6a3-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3e6a3-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e6a3-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3e6a3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e6a3-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e6a3-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e6a3-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3e6a3-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3e6a3-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="3e6a3-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="3e6a3-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3e6a3-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e6a3-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3e6a3-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e6a3-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e6a3-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e6a3-127">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3e6a3-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3e6a3-128">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="3e6a3-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="3e6a3-129">Для этого класса строка имеет значение "./вендор/мсфт/пасспортфорворк/"</span><span class="sxs-lookup"><span data-stu-id="3e6a3-129">For this class, the string is "./Vendor/MSFT/PassportForWork/"</span></span>

</dd> <dt>

[<span data-ttu-id="3e6a3-130">UseBiometrics</span><span class="sxs-lookup"><span data-stu-id="3e6a3-130">UseBiometrics</span></span>](/windows/client-management/mdm/passportforwork-csp#usebiometrics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e6a3-131">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3e6a3-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3e6a3-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3e6a3-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e6a3-133">Требования</span><span class="sxs-lookup"><span data-stu-id="3e6a3-133">Requirements</span></span>



| <span data-ttu-id="3e6a3-134">Требование</span><span class="sxs-lookup"><span data-stu-id="3e6a3-134">Requirement</span></span> | <span data-ttu-id="3e6a3-135">Значение</span><span class="sxs-lookup"><span data-stu-id="3e6a3-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e6a3-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e6a3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3e6a3-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3e6a3-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e6a3-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e6a3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3e6a3-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3e6a3-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3e6a3-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3e6a3-140">Namespace</span></span><br/>                | <span data-ttu-id="3e6a3-141">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="3e6a3-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3e6a3-142">MOF</span><span class="sxs-lookup"><span data-stu-id="3e6a3-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e6a3-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e6a3-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e6a3-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3e6a3-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e6a3-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e6a3-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e6a3-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e6a3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e6a3-147">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="3e6a3-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

