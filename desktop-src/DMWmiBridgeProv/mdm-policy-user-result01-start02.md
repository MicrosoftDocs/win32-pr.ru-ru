---
title: Класс MDM_Policy_User_Result01_Start02
description: '\_ \_ \_ Класс User RESULT01 Start02 политики MDM \_ представляет доступные политики запуска, заданные для каждого пользователя.'
ms.assetid: f7b63db4-f48d-44d2-b343-88cbc8f89cbe
keywords:
- Класс MDM_Policy_User_Result01_Start02
- MDM_Policy_User_Result01_Start02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Start02
- MDM_Policy_User_Result01_Start02.InstanceID
- MDM_Policy_User_Result01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6765a693ef9b4fc579a1bfc5f869db236003801
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489186"
---
# <a name="mdm_policy_user_result01_start02-class"></a><span data-ttu-id="f6295-105">\_Класс политики MDM \_ user \_ Result01 \_ Start02</span><span class="sxs-lookup"><span data-stu-id="f6295-105">MDM\_Policy\_User\_Result01\_Start02 class</span></span>

<span data-ttu-id="f6295-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="f6295-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f6295-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="f6295-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f6295-108">Класс **\_ \_ user \_ Result01 \_ Start02 политики MDM** представляет доступные политики запуска, заданные для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="f6295-108">The **MDM\_Policy\_User\_Result01\_Start02** class represents the start policies available that are set on a per-user basis.</span></span>

<span data-ttu-id="f6295-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f6295-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6295-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6295-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Start02
{
  string InstanceID;
  string ParentID;
  sint32 HidePeopleBar;
  string StartLayout;
};
```

## <a name="members"></a><span data-ttu-id="f6295-111">Члены</span><span class="sxs-lookup"><span data-stu-id="f6295-111">Members</span></span>

<span data-ttu-id="f6295-112">Класс **\_ \_ user \_ Result01 \_ Start02 политики MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f6295-112">The **MDM\_Policy\_User\_Result01\_Start02** class has these types of members:</span></span>

-   [<span data-ttu-id="f6295-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f6295-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f6295-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="f6295-114">Properties</span></span>

<span data-ttu-id="f6295-115">Класс **\_ \_ user \_ Result01 \_ Start02 политики MDM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="f6295-115">The **MDM\_Policy\_User\_Result01\_Start02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f6295-116">HidePeopleBar</span><span class="sxs-lookup"><span data-stu-id="f6295-116">HidePeopleBar</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidepeoplebar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6295-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f6295-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6295-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f6295-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f6295-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f6295-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6295-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f6295-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6295-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f6295-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6295-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f6295-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f6295-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="f6295-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="f6295-124">Для этого класса строка имеет значение Start.</span><span class="sxs-lookup"><span data-stu-id="f6295-124">For this class, the string is "Start"</span></span>

</dd> <dt>

<span data-ttu-id="f6295-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f6295-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6295-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f6295-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6295-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f6295-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6295-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f6295-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f6295-129">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="f6295-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="f6295-130">Для этого класса строка имеет значение "./Усер/вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="f6295-130">For this class, the string is "./User/Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="f6295-131">StartLayout</span><span class="sxs-lookup"><span data-stu-id="f6295-131">StartLayout</span></span>](/windows/client-management/mdm/policy-csp-start#start-startlayout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6295-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f6295-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6295-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f6295-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6295-134">Требования</span><span class="sxs-lookup"><span data-stu-id="f6295-134">Requirements</span></span>



| <span data-ttu-id="f6295-135">Требование</span><span class="sxs-lookup"><span data-stu-id="f6295-135">Requirement</span></span> | <span data-ttu-id="f6295-136">Значение</span><span class="sxs-lookup"><span data-stu-id="f6295-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6295-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6295-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f6295-138">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f6295-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f6295-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6295-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f6295-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f6295-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f6295-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f6295-141">Namespace</span></span><br/>                | <span data-ttu-id="f6295-142">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="f6295-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f6295-143">MOF</span><span class="sxs-lookup"><span data-stu-id="f6295-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6295-144"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6295-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6295-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f6295-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6295-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6295-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6295-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6295-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6295-148">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="f6295-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

