---
description: Описание возможностей связанного Мсвм \_ екстерналесернетпорт.
ms.assetid: 63731b62-b1c7-4dd9-b906-03225bbc3154
title: Класс Msvm_ExternalEthernetPortCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalEthernetPortCapabilities
- Msvm_ExternalEthernetPortCapabilities.InstanceID
- Msvm_ExternalEthernetPortCapabilities.Caption
- Msvm_ExternalEthernetPortCapabilities.Description
- Msvm_ExternalEthernetPortCapabilities.ElementName
- Msvm_ExternalEthernetPortCapabilities.IOVSupport
- Msvm_ExternalEthernetPortCapabilities.IOVSupportReasons
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 748b207151fb1d11b013af7c736de52bbe5bec8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897713"
---
# <a name="msvm_externalethernetportcapabilities-class"></a><span data-ttu-id="ac8e9-103">\_Класс мсвм екстерналесернетпорткапабилитиес</span><span class="sxs-lookup"><span data-stu-id="ac8e9-103">Msvm\_ExternalEthernetPortCapabilities class</span></span>

<span data-ttu-id="ac8e9-104">Описание возможностей связанного [**мсвм \_ екстерналесернетпорт**](msvm-externalethernetport.md).</span><span class="sxs-lookup"><span data-stu-id="ac8e9-104">Describes the capabilities of the associated [**Msvm\_ExternalEthernetPort**](msvm-externalethernetport.md).</span></span>

<span data-ttu-id="ac8e9-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ac8e9-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac8e9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac8e9-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalEthernetPortCapabilities : CIM_Capabilities
{
  string  InstanceID;
  string  Caption = "Ethernet Port Capabilities";
  string  Description = "Describes the capabilities of the Microsoft External Ethernet Port";
  string  ElementName = "Ethernet Port Capabilities";
  boolean IOVSupport;
  string  IOVSupportReasons[];
};
```

## <a name="members"></a><span data-ttu-id="ac8e9-107">Члены</span><span class="sxs-lookup"><span data-stu-id="ac8e9-107">Members</span></span>

<span data-ttu-id="ac8e9-108">Класс **мсвм \_ екстерналесернетпорткапабилитиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ac8e9-108">The **Msvm\_ExternalEthernetPortCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="ac8e9-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="ac8e9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ac8e9-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ac8e9-110">Properties</span></span>

<span data-ttu-id="ac8e9-111">Класс **мсвм \_ екстерналесернетпорткапабилитиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ac8e9-111">The **Msvm\_ExternalEthernetPortCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ac8e9-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="ac8e9-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac8e9-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac8e9-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac8e9-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac8e9-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac8e9-115">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ac8e9-115">A short description of the object.</span></span> <span data-ttu-id="ac8e9-116">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "возможности порта Ethernet".</span><span class="sxs-lookup"><span data-stu-id="ac8e9-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="ac8e9-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ac8e9-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac8e9-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac8e9-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac8e9-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac8e9-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac8e9-120">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ac8e9-120">A description of the object.</span></span> <span data-ttu-id="ac8e9-121">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "описывает возможности внешнего порта Ethernet (Майкрософт)".</span><span class="sxs-lookup"><span data-stu-id="ac8e9-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Describes the capabilities of the Microsoft External Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="ac8e9-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ac8e9-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac8e9-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac8e9-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac8e9-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac8e9-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac8e9-125">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="ac8e9-125">A display name for the object.</span></span> <span data-ttu-id="ac8e9-126">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "возможности порта Ethernet".</span><span class="sxs-lookup"><span data-stu-id="ac8e9-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="ac8e9-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ac8e9-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac8e9-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac8e9-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac8e9-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac8e9-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac8e9-130">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="ac8e9-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ac8e9-131">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="ac8e9-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ac8e9-132">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ac8e9-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ac8e9-133">**иовсуппорт**</span><span class="sxs-lookup"><span data-stu-id="ac8e9-133">**IOVSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac8e9-134">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ac8e9-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac8e9-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac8e9-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac8e9-136">Логическое значение, указывающее, поддерживается ли в сетевом адаптере виртуализация ввода-вывода (IOV).</span><span class="sxs-lookup"><span data-stu-id="ac8e9-136">A boolean value that indicates whether I/O virtualization (IOV) is supported by the network adapter.</span></span> <span data-ttu-id="ac8e9-137">Если значение равно **true**, то поддержка IOV поддерживается сетевым адаптером, а свойство **иовсуппортреасонс** будет пустым.</span><span class="sxs-lookup"><span data-stu-id="ac8e9-137">If the value is **True**, then IOV is supported by the network adapter and the **IOVSupportReasons** property will be empty.</span></span> <span data-ttu-id="ac8e9-138">В противном случае свойство **иовсуппортреасонс** будет иметь причины, по которым невозможно поддерживать IOV.</span><span class="sxs-lookup"><span data-stu-id="ac8e9-138">Otherwise the **IOVSupportReasons** property will have the reasons why IOV cannot be supported.</span></span>

</dd> <dt>

<span data-ttu-id="ac8e9-139">**иовсуппортреасонс**</span><span class="sxs-lookup"><span data-stu-id="ac8e9-139">**IOVSupportReasons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac8e9-140">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ac8e9-140">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ac8e9-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac8e9-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac8e9-142">Массив строк, указывающий возможные причины, по которым не поддерживается IOV.</span><span class="sxs-lookup"><span data-stu-id="ac8e9-142">An array of strings that indicates the possible reasons why IOV is not supported.</span></span> <span data-ttu-id="ac8e9-143">Если значение **иовсуппорт** равно **true**, этот массив будет пустым.</span><span class="sxs-lookup"><span data-stu-id="ac8e9-143">If the value of **IOVSupport** is **True**, this array will be empty.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac8e9-144">Требования</span><span class="sxs-lookup"><span data-stu-id="ac8e9-144">Requirements</span></span>



| <span data-ttu-id="ac8e9-145">Требование</span><span class="sxs-lookup"><span data-stu-id="ac8e9-145">Requirement</span></span> | <span data-ttu-id="ac8e9-146">Значение</span><span class="sxs-lookup"><span data-stu-id="ac8e9-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac8e9-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac8e9-147">Minimum supported client</span></span><br/> | <span data-ttu-id="ac8e9-148">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ac8e9-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ac8e9-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac8e9-149">Minimum supported server</span></span><br/> | <span data-ttu-id="ac8e9-150">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ac8e9-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ac8e9-151">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ac8e9-151">Namespace</span></span><br/>                | <span data-ttu-id="ac8e9-152">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ac8e9-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ac8e9-153">MOF</span><span class="sxs-lookup"><span data-stu-id="ac8e9-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac8e9-154"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac8e9-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac8e9-155">DLL</span><span class="sxs-lookup"><span data-stu-id="ac8e9-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac8e9-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ac8e9-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

