---
title: Класс MDM_Policy_Result01_ErrorReporting02
description: '\_Класс политики MDM \_ Result01 \_ ErrorReporting02 представляет политики отчетов об ошибках.'
ms.assetid: 8cc8c570-70d7-4dcb-a558-122604a14110
keywords:
- Класс MDM_Policy_Result01_ErrorReporting02
- MDM_Policy_Result01_ErrorReporting02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_ErrorReporting02
- MDM_Policy_Result01_ErrorReporting02.InstanceID
- MDM_Policy_Result01_ErrorReporting02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1435e86f4e957a420a76c79f574939cb45df2a4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262196"
---
# <a name="mdm_policy_result01_errorreporting02-class"></a><span data-ttu-id="75f7c-105">\_Класс политики MDM \_ Result01 \_ ErrorReporting02</span><span class="sxs-lookup"><span data-stu-id="75f7c-105">MDM\_Policy\_Result01\_ErrorReporting02 class</span></span>

<span data-ttu-id="75f7c-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="75f7c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="75f7c-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="75f7c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="75f7c-108">\_Класс политики MDM \_ Result01 \_ ErrorReporting02 представляет политики отчетов об ошибках.</span><span class="sxs-lookup"><span data-stu-id="75f7c-108">The MDM\_Policy\_Result01\_ErrorReporting02 class represents the error reporting policies.</span></span>

<span data-ttu-id="75f7c-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="75f7c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="75f7c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75f7c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_ErrorReporting02
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

## <a name="members"></a><span data-ttu-id="75f7c-111">Члены</span><span class="sxs-lookup"><span data-stu-id="75f7c-111">Members</span></span>

<span data-ttu-id="75f7c-112">Класс **\_ политики MDM \_ Result01 \_ ErrorReporting02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="75f7c-112">The **MDM\_Policy\_Result01\_ErrorReporting02** class has these types of members:</span></span>

-   [<span data-ttu-id="75f7c-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="75f7c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="75f7c-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="75f7c-114">Properties</span></span>

<span data-ttu-id="75f7c-115">Класс **\_ политики MDM \_ Result01 \_ ErrorReporting02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="75f7c-115">The **MDM\_Policy\_Result01\_ErrorReporting02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="75f7c-116">кустомизеконсентсеттингс</span><span class="sxs-lookup"><span data-stu-id="75f7c-116">CustomizeConsentSettings</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-customizeconsentsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="75f7c-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="75f7c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75f7c-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75f7c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="75f7c-119">дисаблевиндовсерроррепортинг</span><span class="sxs-lookup"><span data-stu-id="75f7c-119">DisableWindowsErrorReporting</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-disablewindowserrorreporting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="75f7c-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="75f7c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75f7c-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75f7c-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="75f7c-122">дисплайеррорнотификатион</span><span class="sxs-lookup"><span data-stu-id="75f7c-122">DisplayErrorNotification</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-displayerrornotification)
</dt> <dd> <dl> <dt>

<span data-ttu-id="75f7c-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="75f7c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75f7c-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75f7c-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="75f7c-125">донотсендаддитионалдата</span><span class="sxs-lookup"><span data-stu-id="75f7c-125">DoNotSendAdditionalData</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-donotsendadditionaldata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="75f7c-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="75f7c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75f7c-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75f7c-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="75f7c-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="75f7c-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75f7c-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="75f7c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75f7c-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="75f7c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75f7c-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="75f7c-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="75f7c-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="75f7c-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75f7c-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="75f7c-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75f7c-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="75f7c-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75f7c-135">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="75f7c-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="75f7c-136">превенткритикалеррордисплай</span><span class="sxs-lookup"><span data-stu-id="75f7c-136">PreventCriticalErrorDisplay</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-preventcriticalerrordisplay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="75f7c-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="75f7c-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75f7c-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75f7c-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="75f7c-139">Требования</span><span class="sxs-lookup"><span data-stu-id="75f7c-139">Requirements</span></span>



| <span data-ttu-id="75f7c-140">Требование</span><span class="sxs-lookup"><span data-stu-id="75f7c-140">Requirement</span></span> | <span data-ttu-id="75f7c-141">Значение</span><span class="sxs-lookup"><span data-stu-id="75f7c-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75f7c-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="75f7c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="75f7c-143">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="75f7c-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="75f7c-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="75f7c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="75f7c-145">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="75f7c-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="75f7c-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="75f7c-146">Namespace</span></span><br/>                | <span data-ttu-id="75f7c-147">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="75f7c-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="75f7c-148">MOF</span><span class="sxs-lookup"><span data-stu-id="75f7c-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75f7c-149"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75f7c-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="75f7c-150">DLL</span><span class="sxs-lookup"><span data-stu-id="75f7c-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75f7c-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75f7c-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

