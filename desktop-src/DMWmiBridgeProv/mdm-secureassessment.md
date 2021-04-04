---
title: Класс MDM_SecureAssessment
description: MDM \_ секуреассессменткласс используется для предоставления сведений о конфигурации для браузера безопасной оценки.
ms.assetid: ad456f01-c77d-428b-a8bf-03e9ae106e60
keywords:
- Класс MDM_SecureAssessment
- MDM_SecureAssessment класс, описание
topic_type:
- apiref
api_name:
- MDM_SecureAssessment
- MDM_SecureAssessment.InstanceID
- MDM_SecureAssessment.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deef2c8ee832a54775ae9dd51d85414a607ca8b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988224"
---
# <a name="mdm_secureassessment-class"></a><span data-ttu-id="b6839-105">\_Класс MDM секуреассессмент</span><span class="sxs-lookup"><span data-stu-id="b6839-105">MDM\_SecureAssessment class</span></span>

<span data-ttu-id="b6839-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="b6839-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b6839-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="b6839-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b6839-108">Класс **MDM \_ секуреассессмент** используется для предоставления сведений о конфигурации для браузера безопасной оценки.</span><span class="sxs-lookup"><span data-stu-id="b6839-108">The **MDM\_SecureAssessment** class is used to provide configuration information for the secure assessment browser.</span></span>

<span data-ttu-id="b6839-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b6839-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6839-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6839-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_SecureAssessment
{
  string  InstanceID;
  string  ParentID;
  string  LaunchURI;
  string  TesterAccount;
  boolean AllowTextSuggestions;
  boolean RequirePrinting;
  boolean AllowScreenMonitoring;
};
```

## <a name="members"></a><span data-ttu-id="b6839-111">Члены</span><span class="sxs-lookup"><span data-stu-id="b6839-111">Members</span></span>

<span data-ttu-id="b6839-112">Класс **MDM \_ секуреассессмент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b6839-112">The **MDM\_SecureAssessment** class has these types of members:</span></span>

-   [<span data-ttu-id="b6839-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="b6839-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6839-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="b6839-114">Properties</span></span>

<span data-ttu-id="b6839-115">Класс **MDM \_ секуреассессмент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b6839-115">The **MDM\_SecureAssessment** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b6839-116">AllowScreenMonitoring</span><span class="sxs-lookup"><span data-stu-id="b6839-116">AllowScreenMonitoring</span></span>](/windows/client-management/mdm/secureassessment-csp#allowscreenmonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6839-117">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b6839-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b6839-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b6839-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b6839-119">AllowTextSuggestions</span><span class="sxs-lookup"><span data-stu-id="b6839-119">AllowTextSuggestions</span></span>](/windows/client-management/mdm/secureassessment-csp#AllowTextSuggestions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6839-120">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b6839-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b6839-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b6839-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b6839-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b6839-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6839-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b6839-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6839-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b6839-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6839-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b6839-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b6839-126">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="b6839-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="b6839-127">Для этого класса строка имеет значение "Секуреассессмент".</span><span class="sxs-lookup"><span data-stu-id="b6839-127">For this class, the string is "SecureAssessment".</span></span>

</dd> <dt>

[<span data-ttu-id="b6839-128">лаунчури</span><span class="sxs-lookup"><span data-stu-id="b6839-128">LaunchURI</span></span>](/windows/client-management/mdm/secureassessment-csp#launchuri)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6839-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b6839-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6839-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b6839-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b6839-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b6839-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6839-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b6839-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6839-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b6839-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6839-134">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b6839-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b6839-135">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="b6839-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="b6839-136">Для этого класса строка имеет значение "./вендор/мсфт/"</span><span class="sxs-lookup"><span data-stu-id="b6839-136">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="b6839-137">RequirePrinting</span><span class="sxs-lookup"><span data-stu-id="b6839-137">RequirePrinting</span></span>](/windows/client-management/mdm/secureassessment-csp#requireprinting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6839-138">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b6839-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b6839-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b6839-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b6839-140">TesterAccount</span><span class="sxs-lookup"><span data-stu-id="b6839-140">TesterAccount</span></span>](/windows/client-management/mdm/secureassessment-csp#testeraccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6839-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b6839-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6839-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b6839-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6839-143">Требования</span><span class="sxs-lookup"><span data-stu-id="b6839-143">Requirements</span></span>



| <span data-ttu-id="b6839-144">Требование</span><span class="sxs-lookup"><span data-stu-id="b6839-144">Requirement</span></span> | <span data-ttu-id="b6839-145">Значение</span><span class="sxs-lookup"><span data-stu-id="b6839-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6839-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6839-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b6839-147">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b6839-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b6839-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6839-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b6839-149">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b6839-149">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="b6839-150">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b6839-150">Namespace</span></span><br/>                | <span data-ttu-id="b6839-151">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="b6839-151">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="b6839-152">MOF</span><span class="sxs-lookup"><span data-stu-id="b6839-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6839-153"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6839-153"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="b6839-154">DLL</span><span class="sxs-lookup"><span data-stu-id="b6839-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6839-155"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6839-155"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

