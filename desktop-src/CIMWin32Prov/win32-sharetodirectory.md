---
description: '\_Класс WMI взаимосвязей Win32 шаретодиректори связывает общий ресурс в компьютерной системе и каталог, с которым он сопоставлен.'
ms.assetid: f8562539-2cb4-4661-8ef9-8b665e76a292
ms.tgt_platform: multiple
title: Класс Win32_ShareToDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShareToDirectory
- Win32_ShareToDirectory.Share
- Win32_ShareToDirectory.SharedElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f02e5e1ce125a2c8495327a08c14c94ac9f48567
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807018"
---
# <a name="win32_sharetodirectory-class"></a><span data-ttu-id="88dac-103">\_Класс Win32 шаретодиректори</span><span class="sxs-lookup"><span data-stu-id="88dac-103">Win32\_ShareToDirectory class</span></span>

<span data-ttu-id="88dac-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ шаретодиректори** связывает общий ресурс в компьютерной системе и каталог, с которым он сопоставлен.</span><span class="sxs-lookup"><span data-stu-id="88dac-104">The **Win32\_ShareToDirectory** association [WMI class](../wmisdk/retrieving-a-class.md) relates a shared resource on the computer system and the directory to which it is mapped.</span></span>

<span data-ttu-id="88dac-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="88dac-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="88dac-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="88dac-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="88dac-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88dac-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{8502C511-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ShareToDirectory
{
  Win32_Share   REF Share;
  CIM_Directory REF SharedElement;
};
```

## <a name="members"></a><span data-ttu-id="88dac-108">Члены</span><span class="sxs-lookup"><span data-stu-id="88dac-108">Members</span></span>

<span data-ttu-id="88dac-109">Класс **Win32 \_ шаретодиректори** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="88dac-109">The **Win32\_ShareToDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="88dac-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="88dac-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="88dac-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="88dac-111">Properties</span></span>

<span data-ttu-id="88dac-112">Класс **Win32 \_ шаретодиректори** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="88dac-112">The **Win32\_ShareToDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88dac-113">**Предоставить общий доступ**</span><span class="sxs-lookup"><span data-stu-id="88dac-113">**Share**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88dac-114">Тип данных: **\_ общий ресурс Win32**</span><span class="sxs-lookup"><span data-stu-id="88dac-114">Data type: **Win32\_Share**</span></span>
</dt> <dt>

<span data-ttu-id="88dac-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88dac-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88dac-116">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| \_ общий ресурс Win32 WMI")</span><span class="sxs-lookup"><span data-stu-id="88dac-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Share")</span></span>
</dt> </dl>

<span data-ttu-id="88dac-117">Ссылка на экземпляр, представляющий свойства общего ресурса, доступного через каталог.</span><span class="sxs-lookup"><span data-stu-id="88dac-117">Reference to the instance representing the properties of a shared resource available through the directory.</span></span>

</dd> <dt>

<span data-ttu-id="88dac-118">**шаределемент**</span><span class="sxs-lookup"><span data-stu-id="88dac-118">**SharedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88dac-119">Тип данных: **\_ Каталог CIM**</span><span class="sxs-lookup"><span data-stu-id="88dac-119">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="88dac-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88dac-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88dac-121">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ Directory")</span><span class="sxs-lookup"><span data-stu-id="88dac-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="88dac-122">Ссылка на экземпляр, представляющий свойства каталога, сопоставленного с общим ресурсом.</span><span class="sxs-lookup"><span data-stu-id="88dac-122">Reference to the instance representing the properties of the directory that has been mapped to a shared resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88dac-123">Требования</span><span class="sxs-lookup"><span data-stu-id="88dac-123">Requirements</span></span>



| <span data-ttu-id="88dac-124">Требование</span><span class="sxs-lookup"><span data-stu-id="88dac-124">Requirement</span></span> | <span data-ttu-id="88dac-125">Значение</span><span class="sxs-lookup"><span data-stu-id="88dac-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88dac-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88dac-126">Minimum supported client</span></span><br/> | <span data-ttu-id="88dac-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88dac-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="88dac-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88dac-128">Minimum supported server</span></span><br/> | <span data-ttu-id="88dac-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88dac-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="88dac-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="88dac-130">Namespace</span></span><br/>                | <span data-ttu-id="88dac-131">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="88dac-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="88dac-132">MOF</span><span class="sxs-lookup"><span data-stu-id="88dac-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88dac-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88dac-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="88dac-134">DLL</span><span class="sxs-lookup"><span data-stu-id="88dac-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88dac-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88dac-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88dac-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88dac-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88dac-137">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="88dac-137">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
