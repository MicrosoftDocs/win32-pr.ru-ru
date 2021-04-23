---
title: Класс MDM_Policy_Result01_Maps02
description: '\_Класс политики MDM \_ Result01 \_ Maps02 представляет доступные политики отображения.'
ms.assetid: 09a2755c-1d2c-4c34-a5e7-d8fc07b55ad8
keywords:
- Класс MDM_Policy_Result01_Maps02
- MDM_Policy_Result01_Maps02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Maps02
- MDM_Policy_Result01_Maps02.InstanceID
- MDM_Policy_Result01_Maps02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7bc3676a8c2900cba6afcbeff20839153ec3320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490161"
---
# <a name="mdm_policy_result01_maps02-class"></a><span data-ttu-id="d04e6-105">\_Класс политики MDM \_ Result01 \_ Maps02</span><span class="sxs-lookup"><span data-stu-id="d04e6-105">MDM\_Policy\_Result01\_Maps02 class</span></span>

<span data-ttu-id="d04e6-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="d04e6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d04e6-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="d04e6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d04e6-108">Класс **\_ политики MDM \_ Result01 \_ Maps02** представляет доступные политики отображения.</span><span class="sxs-lookup"><span data-stu-id="d04e6-108">The **MDM\_Policy\_Result01\_Maps02** class represents the map policies available.</span></span>

<span data-ttu-id="d04e6-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="d04e6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d04e6-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d04e6-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Maps02
{
  string InstanceID;
  string ParentID;
  sint32 AllowOfflineMapsDownloadOverMeteredConnection;
  sint32 EnableOfflineMapsAutoUpdate;
};
```

## <a name="members"></a><span data-ttu-id="d04e6-111">Члены</span><span class="sxs-lookup"><span data-stu-id="d04e6-111">Members</span></span>

<span data-ttu-id="d04e6-112">Класс **\_ политики MDM \_ Result01 \_ Maps02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d04e6-112">The **MDM\_Policy\_Result01\_Maps02** class has these types of members:</span></span>

-   [<span data-ttu-id="d04e6-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="d04e6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d04e6-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="d04e6-114">Properties</span></span>

<span data-ttu-id="d04e6-115">Класс **\_ политики MDM \_ Result01 \_ Maps02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d04e6-115">The **MDM\_Policy\_Result01\_Maps02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d04e6-116">алловоффлинемапсдовнлоадоверметередконнектион</span><span class="sxs-lookup"><span data-stu-id="d04e6-116">AllowOfflineMapsDownloadOverMeteredConnection</span></span>](/windows/client-management/mdm/policy-csp-maps#maps-allowofflinemapsdownloadovermeteredconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d04e6-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="d04e6-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d04e6-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d04e6-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d04e6-119">енаблеоффлинемапсаутаупдате</span><span class="sxs-lookup"><span data-stu-id="d04e6-119">EnableOfflineMapsAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-maps#maps-enableofflinemapsautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d04e6-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="d04e6-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d04e6-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d04e6-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d04e6-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d04e6-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d04e6-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d04e6-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d04e6-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d04e6-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d04e6-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d04e6-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d04e6-126">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="d04e6-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="d04e6-127">Для этого класса строка имеет значение "Maps".</span><span class="sxs-lookup"><span data-stu-id="d04e6-127">For this class, the string is "Maps".</span></span>

</dd> <dt>

<span data-ttu-id="d04e6-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d04e6-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d04e6-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d04e6-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d04e6-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d04e6-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d04e6-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d04e6-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d04e6-132">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="d04e6-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="d04e6-133">Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="d04e6-133">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d04e6-134">Требования</span><span class="sxs-lookup"><span data-stu-id="d04e6-134">Requirements</span></span>



| <span data-ttu-id="d04e6-135">Требование</span><span class="sxs-lookup"><span data-stu-id="d04e6-135">Requirement</span></span> | <span data-ttu-id="d04e6-136">Значение</span><span class="sxs-lookup"><span data-stu-id="d04e6-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d04e6-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d04e6-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d04e6-138">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d04e6-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d04e6-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d04e6-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d04e6-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d04e6-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="d04e6-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d04e6-141">Namespace</span></span><br/>                | <span data-ttu-id="d04e6-142">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="d04e6-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="d04e6-143">MOF</span><span class="sxs-lookup"><span data-stu-id="d04e6-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d04e6-144"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d04e6-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="d04e6-145">DLL</span><span class="sxs-lookup"><span data-stu-id="d04e6-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d04e6-146"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d04e6-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

