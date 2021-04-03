---
description: '\_Класс WMI взаимосвязей Win32 протоколбиндинг связывает драйвер системного уровня, Сетевой протокол и сетевой адаптер.'
ms.assetid: 09b84bb2-9999-4e80-a330-88ed6b2bd5e9
ms.tgt_platform: multiple
title: Класс Win32_ProtocolBinding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProtocolBinding
- Win32_ProtocolBinding.Antecedent
- Win32_ProtocolBinding.Dependent
- Win32_ProtocolBinding.Device
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 91e735a599a1dda2536fe26bcd654dcdf4b119dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895461"
---
# <a name="win32_protocolbinding-class"></a><span data-ttu-id="147a3-103">\_Класс Win32 протоколбиндинг</span><span class="sxs-lookup"><span data-stu-id="147a3-103">Win32\_ProtocolBinding class</span></span>

<span data-ttu-id="147a3-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ протоколбиндинг** связывает драйвер системного уровня, Сетевой протокол и сетевой адаптер.</span><span class="sxs-lookup"><span data-stu-id="147a3-104">The **Win32\_ProtocolBinding** association [WMI class](../wmisdk/retrieving-a-class.md) relates a system-level driver, network protocol, and network adapter.</span></span>

<span data-ttu-id="147a3-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="147a3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="147a3-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="147a3-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="147a3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="147a3-107">Syntax</span></span>

``` syntax
[Dynamic, Association, Provider("CIMWin32"), UUID("{8502C509-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProtocolBinding
{
  Win32_NetworkProtocol REF Antecedent;
  Win32_SystemDriver    REF Dependent;
  Win32_NetworkAdapter  REF Device;
};
```

## <a name="members"></a><span data-ttu-id="147a3-108">Члены</span><span class="sxs-lookup"><span data-stu-id="147a3-108">Members</span></span>

<span data-ttu-id="147a3-109">Класс **Win32 \_ протоколбиндинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="147a3-109">The **Win32\_ProtocolBinding** class has these types of members:</span></span>

-   [<span data-ttu-id="147a3-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="147a3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="147a3-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="147a3-111">Properties</span></span>

<span data-ttu-id="147a3-112">Класс **Win32 \_ протоколбиндинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="147a3-112">The **Win32\_ProtocolBinding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="147a3-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="147a3-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a3-114">Тип данных: **Win32 \_ NetworkProtocol**</span><span class="sxs-lookup"><span data-stu-id="147a3-114">Data type: **Win32\_NetworkProtocol**</span></span>
</dt> <dt>

<span data-ttu-id="147a3-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="147a3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a3-116">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkProtocol")</span><span class="sxs-lookup"><span data-stu-id="147a3-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkProtocol")</span></span>
</dt> </dl>

<span data-ttu-id="147a3-117">Ссылка на экземпляр, представляющий протокол, используемый с системным драйвером и сетевым адаптером.</span><span class="sxs-lookup"><span data-stu-id="147a3-117">Reference to the instance representing the protocol that is used with the system driver and on the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="147a3-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="147a3-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a3-119">Тип данных: **Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="147a3-119">Data type: **Win32\_SystemDriver**</span></span>
</dt> <dt>

<span data-ttu-id="147a3-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="147a3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a3-121">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SystemDriver")</span><span class="sxs-lookup"><span data-stu-id="147a3-121">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SystemDriver")</span></span>
</dt> </dl>

<span data-ttu-id="147a3-122">Ссылка на экземпляр, представляющий системный драйвер, использующий сетевой адаптер через сетевой протокол этого класса.</span><span class="sxs-lookup"><span data-stu-id="147a3-122">Reference to the instance representing the system driver that uses the network adapter through the network protocol of this class.</span></span>

</dd> <dt>

<span data-ttu-id="147a3-123">**Устройство**</span><span class="sxs-lookup"><span data-stu-id="147a3-123">**Device**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a3-124">Тип данных: **Win32 \_ сетевого адаптера**</span><span class="sxs-lookup"><span data-stu-id="147a3-124">Data type: **Win32\_NetworkAdapter**</span></span>
</dt> <dt>

<span data-ttu-id="147a3-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="147a3-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a3-126">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ сетевого адаптера")</span><span class="sxs-lookup"><span data-stu-id="147a3-126">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapter")</span></span>
</dt> </dl>

<span data-ttu-id="147a3-127">Свойства сетевого адаптера, используемого в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="147a3-127">Properties of the network adapter being used on the computer system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="147a3-128">Требования</span><span class="sxs-lookup"><span data-stu-id="147a3-128">Requirements</span></span>



| <span data-ttu-id="147a3-129">Требование</span><span class="sxs-lookup"><span data-stu-id="147a3-129">Requirement</span></span> | <span data-ttu-id="147a3-130">Значение</span><span class="sxs-lookup"><span data-stu-id="147a3-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="147a3-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="147a3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="147a3-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="147a3-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="147a3-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="147a3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="147a3-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="147a3-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="147a3-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="147a3-135">Namespace</span></span><br/>                | <span data-ttu-id="147a3-136">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="147a3-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="147a3-137">MOF</span><span class="sxs-lookup"><span data-stu-id="147a3-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="147a3-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="147a3-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="147a3-139">DLL</span><span class="sxs-lookup"><span data-stu-id="147a3-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="147a3-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="147a3-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="147a3-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="147a3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="147a3-142">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="147a3-142">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
