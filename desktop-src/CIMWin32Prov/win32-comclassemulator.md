---
description: '\_Класс WMI взаимосвязей Win32 комклассемулатор связывает две версии класса модели COM.'
ms.assetid: 33899c1e-911d-49ad-be25-355dcdb8f0c7
ms.tgt_platform: multiple
title: Класс Win32_ComClassEmulator
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComClassEmulator
- Win32_ComClassEmulator.NewVersion
- Win32_ComClassEmulator.OldVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9966ed85b0e0b4eeb25073e13ad679759f1d460b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141058"
---
# <a name="win32_comclassemulator-class"></a><span data-ttu-id="916ca-103">\_Класс Win32 комклассемулатор</span><span class="sxs-lookup"><span data-stu-id="916ca-103">Win32\_ComClassEmulator class</span></span>

<span data-ttu-id="916ca-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ комклассемулатор** связывает две версии класса модели COM.</span><span class="sxs-lookup"><span data-stu-id="916ca-104">The **Win32\_ComClassEmulator** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates two versions of a Component Object Model (COM) class.</span></span>

<span data-ttu-id="916ca-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="916ca-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="916ca-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="916ca-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="916ca-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="916ca-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5C-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComClassEmulator
{
  Win32_ClassicCOMClass REF NewVersion;
  Win32_ClassicCOMClass REF OldVersion;
};
```

## <a name="members"></a><span data-ttu-id="916ca-108">Члены</span><span class="sxs-lookup"><span data-stu-id="916ca-108">Members</span></span>

<span data-ttu-id="916ca-109">Класс **Win32 \_ комклассемулатор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="916ca-109">The **Win32\_ComClassEmulator** class has these types of members:</span></span>

-   [<span data-ttu-id="916ca-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="916ca-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="916ca-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="916ca-111">Properties</span></span>

<span data-ttu-id="916ca-112">Класс **Win32 \_ комклассемулатор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="916ca-112">The **Win32\_ComClassEmulator** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="916ca-113">**NewVersion**</span><span class="sxs-lookup"><span data-stu-id="916ca-113">**NewVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="916ca-114">Тип данных: **Win32 \_ классиккомкласс**</span><span class="sxs-lookup"><span data-stu-id="916ca-114">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="916ca-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="916ca-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="916ca-116">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ классиккомкласс")</span><span class="sxs-lookup"><span data-stu-id="916ca-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="916ca-117">Ссылка на экземпляр, представляющий COM-компонент, который содержит интерфейсы, имитирующие старую версию компонента.</span><span class="sxs-lookup"><span data-stu-id="916ca-117">Reference to the instance representing the COM component that contains interfaces emulating the older version of the component.</span></span>

</dd> <dt>

<span data-ttu-id="916ca-118">**OldVersion**</span><span class="sxs-lookup"><span data-stu-id="916ca-118">**OldVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="916ca-119">Тип данных: **Win32 \_ классиккомкласс**</span><span class="sxs-lookup"><span data-stu-id="916ca-119">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="916ca-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="916ca-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="916ca-121">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ классиккомкласс")</span><span class="sxs-lookup"><span data-stu-id="916ca-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="916ca-122">Ссылка на экземпляр, представляющий COM-компонент с интерфейсами, которые могут эмулироваться новой версией компонента.</span><span class="sxs-lookup"><span data-stu-id="916ca-122">Reference to the instance representing the COM component with interfaces that can be emulated by the new version of the component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="916ca-123">Требования</span><span class="sxs-lookup"><span data-stu-id="916ca-123">Requirements</span></span>



| <span data-ttu-id="916ca-124">Требование</span><span class="sxs-lookup"><span data-stu-id="916ca-124">Requirement</span></span> | <span data-ttu-id="916ca-125">Значение</span><span class="sxs-lookup"><span data-stu-id="916ca-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="916ca-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="916ca-126">Minimum supported client</span></span><br/> | <span data-ttu-id="916ca-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="916ca-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="916ca-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="916ca-128">Minimum supported server</span></span><br/> | <span data-ttu-id="916ca-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="916ca-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="916ca-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="916ca-130">Namespace</span></span><br/>                | <span data-ttu-id="916ca-131">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="916ca-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="916ca-132">MOF</span><span class="sxs-lookup"><span data-stu-id="916ca-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="916ca-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="916ca-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="916ca-134">DLL</span><span class="sxs-lookup"><span data-stu-id="916ca-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="916ca-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="916ca-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="916ca-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="916ca-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="916ca-137">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="916ca-137">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

