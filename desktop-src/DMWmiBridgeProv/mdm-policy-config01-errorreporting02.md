---
title: Класс MDM_Policy_Config01_ErrorReporting02
description: '\_Класс политики MDM \_ Config01 \_ ErrorReporting02 настраивает политики отчетов об ошибках.'
ms.assetid: 41067b5e-0db5-43b3-b1d5-2d6c54c35388
keywords:
- Класс MDM_Policy_Config01_ErrorReporting02
- MDM_Policy_Config01_ErrorReporting02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ErrorReporting02
- MDM_Policy_Config01_ErrorReporting02.InstanceID
- MDM_Policy_Config01_ErrorReporting02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1c23cf5b0b01f05fa3712d6b1de11461c6f47da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071427"
---
# <a name="mdm_policy_config01_errorreporting02-class"></a><span data-ttu-id="a5e6a-105">\_Класс политики MDM \_ Config01 \_ ErrorReporting02</span><span class="sxs-lookup"><span data-stu-id="a5e6a-105">MDM\_Policy\_Config01\_ErrorReporting02 class</span></span>

<span data-ttu-id="a5e6a-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="a5e6a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a5e6a-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="a5e6a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a5e6a-108">\_Класс политики MDM \_ Config01 \_ ErrorReporting02 настраивает политики отчетов об ошибках.</span><span class="sxs-lookup"><span data-stu-id="a5e6a-108">The MDM\_Policy\_Config01\_ErrorReporting02 class configures the error reporting policies.</span></span>

<span data-ttu-id="a5e6a-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="a5e6a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5e6a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5e6a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ErrorReporting02
{
  string InstanceID;
  string ParentID;
  string CustomizeConsentSettings;
  string DisableWindowsErrorReporting;
  string DisplayErrorNotification;
  string DoNotSendAdditionalData;
  string PreventCriticalErrorDisplay;
};
```

## <a name="members"></a><span data-ttu-id="a5e6a-111">Члены</span><span class="sxs-lookup"><span data-stu-id="a5e6a-111">Members</span></span>

<span data-ttu-id="a5e6a-112">Класс **\_ политики MDM \_ Config01 \_ ErrorReporting02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a5e6a-112">The **MDM\_Policy\_Config01\_ErrorReporting02** class has these types of members:</span></span>

-   [<span data-ttu-id="a5e6a-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="a5e6a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5e6a-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="a5e6a-114">Properties</span></span>

<span data-ttu-id="a5e6a-115">Класс **\_ политики MDM \_ Config01 \_ ErrorReporting02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a5e6a-115">The **MDM\_Policy\_Config01\_ErrorReporting02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a5e6a-116">кустомизеконсентсеттингс</span><span class="sxs-lookup"><span data-stu-id="a5e6a-116">CustomizeConsentSettings</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-customizeconsentsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5e6a-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a5e6a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5e6a-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a5e6a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a5e6a-119">дисаблевиндовсерроррепортинг</span><span class="sxs-lookup"><span data-stu-id="a5e6a-119">DisableWindowsErrorReporting</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-disablewindowserrorreporting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5e6a-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a5e6a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5e6a-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a5e6a-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a5e6a-122">дисплайеррорнотификатион</span><span class="sxs-lookup"><span data-stu-id="a5e6a-122">DisplayErrorNotification</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-displayerrornotification)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5e6a-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a5e6a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5e6a-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a5e6a-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a5e6a-125">донотсендаддитионалдата</span><span class="sxs-lookup"><span data-stu-id="a5e6a-125">DoNotSendAdditionalData</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-donotsendadditionaldata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5e6a-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a5e6a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5e6a-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a5e6a-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a5e6a-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a5e6a-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5e6a-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a5e6a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5e6a-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5e6a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5e6a-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a5e6a-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a5e6a-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a5e6a-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5e6a-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a5e6a-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5e6a-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5e6a-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5e6a-135">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a5e6a-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a5e6a-136">превенткритикалеррордисплай</span><span class="sxs-lookup"><span data-stu-id="a5e6a-136">PreventCriticalErrorDisplay</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-preventcriticalerrordisplay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5e6a-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a5e6a-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5e6a-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a5e6a-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5e6a-139">Требования</span><span class="sxs-lookup"><span data-stu-id="a5e6a-139">Requirements</span></span>



| <span data-ttu-id="a5e6a-140">Требование</span><span class="sxs-lookup"><span data-stu-id="a5e6a-140">Requirement</span></span> | <span data-ttu-id="a5e6a-141">Значение</span><span class="sxs-lookup"><span data-stu-id="a5e6a-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5e6a-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5e6a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a5e6a-143">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a5e6a-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a5e6a-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5e6a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a5e6a-145">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a5e6a-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a5e6a-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a5e6a-146">Namespace</span></span><br/>                | <span data-ttu-id="a5e6a-147">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="a5e6a-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a5e6a-148">MOF</span><span class="sxs-lookup"><span data-stu-id="a5e6a-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5e6a-149"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5e6a-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5e6a-150">DLL</span><span class="sxs-lookup"><span data-stu-id="a5e6a-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5e6a-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5e6a-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

