---
description: Абстрактный класс, представляющий параметры для определенной функции системы или компонента.
ms.assetid: f55eacdd-a802-4374-8756-a59733af6d2c
title: Класс Msvm_FeatureSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FeatureSettingData
- Msvm_FeatureSettingData.InstanceID
- Msvm_FeatureSettingData.Caption
- Msvm_FeatureSettingData.Description
- Msvm_FeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98f022515ac877c0dd598cb9a962bc3133f76eb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540338"
---
# <a name="msvm_featuresettingdata-class"></a><span data-ttu-id="c17bb-103">\_Класс мсвм феатуресеттингдата</span><span class="sxs-lookup"><span data-stu-id="c17bb-103">Msvm\_FeatureSettingData class</span></span>

<span data-ttu-id="c17bb-104">Абстрактный класс, представляющий параметры для определенной функции системы или компонента.</span><span class="sxs-lookup"><span data-stu-id="c17bb-104">An abstract class that represents settings for a specific feature of a system or component.</span></span>

<span data-ttu-id="c17bb-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c17bb-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c17bb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c17bb-106">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FeatureSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="c17bb-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c17bb-107">Members</span></span>

<span data-ttu-id="c17bb-108">Класс **мсвм \_ феатуресеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c17bb-108">The **Msvm\_FeatureSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c17bb-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="c17bb-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c17bb-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c17bb-110">Properties</span></span>

<span data-ttu-id="c17bb-111">Класс **мсвм \_ феатуресеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c17bb-111">The **Msvm\_FeatureSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c17bb-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c17bb-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c17bb-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c17bb-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c17bb-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c17bb-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c17bb-115">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c17bb-115">A short description of the object.</span></span> <span data-ttu-id="c17bb-116">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c17bb-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c17bb-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c17bb-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c17bb-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c17bb-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c17bb-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c17bb-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c17bb-120">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c17bb-120">A description of the object.</span></span> <span data-ttu-id="c17bb-121">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c17bb-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c17bb-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c17bb-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c17bb-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c17bb-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c17bb-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c17bb-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c17bb-125">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="c17bb-125">A display name for the object.</span></span> <span data-ttu-id="c17bb-126">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c17bb-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c17bb-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c17bb-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c17bb-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c17bb-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c17bb-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c17bb-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c17bb-130">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="c17bb-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c17bb-131">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="c17bb-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c17bb-132">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c17bb-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c17bb-133">Требования</span><span class="sxs-lookup"><span data-stu-id="c17bb-133">Requirements</span></span>



| <span data-ttu-id="c17bb-134">Требование</span><span class="sxs-lookup"><span data-stu-id="c17bb-134">Requirement</span></span> | <span data-ttu-id="c17bb-135">Значение</span><span class="sxs-lookup"><span data-stu-id="c17bb-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c17bb-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c17bb-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c17bb-137">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c17bb-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c17bb-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c17bb-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c17bb-139">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c17bb-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c17bb-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c17bb-140">Namespace</span></span><br/>                | <span data-ttu-id="c17bb-141">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c17bb-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c17bb-142">MOF</span><span class="sxs-lookup"><span data-stu-id="c17bb-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c17bb-143"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c17bb-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c17bb-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c17bb-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c17bb-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c17bb-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

