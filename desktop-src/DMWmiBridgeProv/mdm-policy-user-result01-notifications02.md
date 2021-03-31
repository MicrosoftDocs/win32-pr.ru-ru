---
title: Класс MDM_Policy_User_Result01_Notifications02
description: '\_Класс политики MDM \_ user \_ Result01 \_ Notifications02 представляет доступные политики уведомлений.'
ms.assetid: a2da74f3-2585-4c8c-abab-751ba4c708a1
keywords:
- Класс MDM_Policy_User_Result01_Notifications02
- MDM_Policy_User_Result01_Notifications02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Notifications02
- MDM_Policy_User_Result01_Notifications02.InstanceID
- MDM_Policy_User_Result01_Notifications02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c917e42ef568783b1c804ce17d52474a86359e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071164"
---
# <a name="mdm_policy_user_result01_notifications02-class"></a><span data-ttu-id="8c859-105">\_Класс политики MDM \_ user \_ Result01 \_ Notifications02</span><span class="sxs-lookup"><span data-stu-id="8c859-105">MDM\_Policy\_User\_Result01\_Notifications02 class</span></span>

<span data-ttu-id="8c859-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="8c859-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8c859-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="8c859-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8c859-108">Класс **\_ политики MDM \_ user \_ Result01 \_ Notifications02** представляет доступные политики уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8c859-108">The **MDM\_Policy\_User\_Result01\_Notifications02** class represents the notification policies available.</span></span>

<span data-ttu-id="8c859-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="8c859-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c859-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c859-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Notifications02
{
  string InstanceID;
  string ParentID;
  sint32 DisallowNotificationMirroring;
};
```

## <a name="members"></a><span data-ttu-id="8c859-111">Члены</span><span class="sxs-lookup"><span data-stu-id="8c859-111">Members</span></span>

<span data-ttu-id="8c859-112">Класс **\_ \_ user \_ Result01 \_ Notifications02 политики MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8c859-112">The **MDM\_Policy\_User\_Result01\_Notifications02** class has these types of members:</span></span>

-   [<span data-ttu-id="8c859-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="8c859-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c859-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="8c859-114">Properties</span></span>

<span data-ttu-id="8c859-115">Класс **\_ \_ user \_ Result01 \_ Notifications02 политики MDM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="8c859-115">The **MDM\_Policy\_User\_Result01\_Notifications02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8c859-116">дисалловнотификатионмирроринг</span><span class="sxs-lookup"><span data-stu-id="8c859-116">DisallowNotificationMirroring</span></span>](/windows/client-management/mdm/policy-csp-notifications#notifications-disallownotificationmirroring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c859-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8c859-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c859-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8c859-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8c859-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8c859-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c859-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8c859-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c859-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8c859-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c859-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8c859-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8c859-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="8c859-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="8c859-124">Для этого класса строка имеет значение "Notifications".</span><span class="sxs-lookup"><span data-stu-id="8c859-124">For this class, the string is "Notifications".</span></span>

</dd> <dt>

<span data-ttu-id="8c859-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8c859-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c859-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8c859-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c859-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8c859-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c859-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8c859-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8c859-129">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="8c859-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="8c859-130">Для этого класса строка имеет значение "./Усер/вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="8c859-130">For this class, the string is "./User/Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c859-131">Требования</span><span class="sxs-lookup"><span data-stu-id="8c859-131">Requirements</span></span>



| <span data-ttu-id="8c859-132">Требование</span><span class="sxs-lookup"><span data-stu-id="8c859-132">Requirement</span></span> | <span data-ttu-id="8c859-133">Значение</span><span class="sxs-lookup"><span data-stu-id="8c859-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c859-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c859-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8c859-135">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8c859-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8c859-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c859-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8c859-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8c859-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="8c859-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8c859-138">Namespace</span></span><br/>                | <span data-ttu-id="8c859-139">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="8c859-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="8c859-140">MOF</span><span class="sxs-lookup"><span data-stu-id="8c859-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c859-141"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c859-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="8c859-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8c859-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c859-143"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c859-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

