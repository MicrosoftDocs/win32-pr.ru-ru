---
description: Абстрактный базовый класс для классов, представляющих параметры для функции порта коммутатора Ethernet.
ms.assetid: 26c40dd0-fe1e-4432-a177-8a565bf678e6
title: Класс Msvm_EthernetSwitchPortFeatureSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortFeatureSettingData
- Msvm_EthernetSwitchPortFeatureSettingData.InstanceID
- Msvm_EthernetSwitchPortFeatureSettingData.Caption
- Msvm_EthernetSwitchPortFeatureSettingData.Description
- Msvm_EthernetSwitchPortFeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0734fa89d99d80e26e4d5fc841bdac89cfd8dfe6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346062"
---
# <a name="msvm_ethernetswitchportfeaturesettingdata-class"></a><span data-ttu-id="c49df-103">\_Класс мсвм есернетсвитчпортфеатуресеттингдата</span><span class="sxs-lookup"><span data-stu-id="c49df-103">Msvm\_EthernetSwitchPortFeatureSettingData class</span></span>

<span data-ttu-id="c49df-104">Абстрактный базовый класс для классов, представляющих параметры для функции порта коммутатора Ethernet.</span><span class="sxs-lookup"><span data-stu-id="c49df-104">Abstract base class for classes that represent settings for an Ethernet switch port feature.</span></span>

<span data-ttu-id="c49df-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c49df-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c49df-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c49df-106">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchPortFeatureSettingData : Msvm_FeatureSettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="c49df-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c49df-107">Members</span></span>

<span data-ttu-id="c49df-108">Класс **мсвм \_ есернетсвитчпортфеатуресеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c49df-108">The **Msvm\_EthernetSwitchPortFeatureSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c49df-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="c49df-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c49df-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c49df-110">Properties</span></span>

<span data-ttu-id="c49df-111">Класс **мсвм \_ есернетсвитчпортфеатуресеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c49df-111">The **Msvm\_EthernetSwitchPortFeatureSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c49df-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c49df-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c49df-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c49df-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c49df-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c49df-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c49df-115">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c49df-115">A short description of the object.</span></span> <span data-ttu-id="c49df-116">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c49df-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c49df-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c49df-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c49df-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c49df-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c49df-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c49df-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c49df-120">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c49df-120">A description of the object.</span></span> <span data-ttu-id="c49df-121">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c49df-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c49df-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c49df-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c49df-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c49df-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c49df-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c49df-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c49df-125">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="c49df-125">A display name for the object.</span></span> <span data-ttu-id="c49df-126">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c49df-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c49df-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c49df-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c49df-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c49df-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c49df-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c49df-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c49df-130">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="c49df-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c49df-131">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="c49df-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c49df-132">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c49df-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c49df-133">Требования</span><span class="sxs-lookup"><span data-stu-id="c49df-133">Requirements</span></span>



| <span data-ttu-id="c49df-134">Требование</span><span class="sxs-lookup"><span data-stu-id="c49df-134">Requirement</span></span> | <span data-ttu-id="c49df-135">Значение</span><span class="sxs-lookup"><span data-stu-id="c49df-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c49df-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c49df-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c49df-137">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c49df-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c49df-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c49df-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c49df-139">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c49df-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c49df-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c49df-140">Namespace</span></span><br/>                | <span data-ttu-id="c49df-141">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c49df-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c49df-142">MOF</span><span class="sxs-lookup"><span data-stu-id="c49df-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c49df-143"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c49df-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c49df-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c49df-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c49df-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c49df-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

