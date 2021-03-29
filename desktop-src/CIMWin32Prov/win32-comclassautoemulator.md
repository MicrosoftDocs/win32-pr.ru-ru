---
description: '\_Класс WMI взаимосвязей Win32 комклассаутоемулатор связывает класс модели COM и другой класс COM, который он автоматически эмулирует.'
ms.assetid: e060ba26-98e7-47cb-bf21-1ca80d0e8a07
ms.tgt_platform: multiple
title: Класс Win32_ComClassAutoEmulator
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComClassAutoEmulator
- Win32_ComClassAutoEmulator.NewVersion
- Win32_ComClassAutoEmulator.OldVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9442036d43859caa5fa277109c7e85553e7d42f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142295"
---
# <a name="win32_comclassautoemulator-class"></a><span data-ttu-id="d2274-103">\_Класс Win32 комклассаутоемулатор</span><span class="sxs-lookup"><span data-stu-id="d2274-103">Win32\_ComClassAutoEmulator class</span></span>

<span data-ttu-id="d2274-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ КОМКЛАССАУТОЕМУЛАТОР** связывает класс модели COM и другой класс COM, который он автоматически эмулирует.</span><span class="sxs-lookup"><span data-stu-id="d2274-104">The **Win32\_ComClassAutoEmulator** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a Component Object Model (COM) class and another COM class that it automatically emulates.</span></span>

<span data-ttu-id="d2274-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d2274-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d2274-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="d2274-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2274-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2274-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5D-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComClassAutoEmulator
{
  Win32_ClassicCOMClass REF NewVersion;
  Win32_ClassicCOMClass REF OldVersion;
};
```

## <a name="members"></a><span data-ttu-id="d2274-108">Члены</span><span class="sxs-lookup"><span data-stu-id="d2274-108">Members</span></span>

<span data-ttu-id="d2274-109">Класс **Win32 \_ комклассаутоемулатор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d2274-109">The **Win32\_ComClassAutoEmulator** class has these types of members:</span></span>

-   [<span data-ttu-id="d2274-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d2274-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d2274-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="d2274-111">Properties</span></span>

<span data-ttu-id="d2274-112">Класс **Win32 \_ комклассаутоемулатор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d2274-112">The **Win32\_ComClassAutoEmulator** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d2274-113">**NewVersion**</span><span class="sxs-lookup"><span data-stu-id="d2274-113">**NewVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2274-114">Тип данных: **Win32 \_ классиккомкласс**</span><span class="sxs-lookup"><span data-stu-id="d2274-114">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="d2274-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d2274-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2274-116">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ классиккомкласс")</span><span class="sxs-lookup"><span data-stu-id="d2274-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="d2274-117">Ссылка на экземпляр, представляющий COM-компонент, который может автоматически эмулировать связанный COM-компонент.</span><span class="sxs-lookup"><span data-stu-id="d2274-117">Reference to the instance representing the COM component that can automatically emulate the associated COM component.</span></span> <span data-ttu-id="d2274-118">Эти сведения извлекаются с помощью записи реестра Аутотреатас.</span><span class="sxs-lookup"><span data-stu-id="d2274-118">This information is obtained through the AutoTreatAs registry entry.</span></span>

</dd> <dt>

<span data-ttu-id="d2274-119">**OldVersion**</span><span class="sxs-lookup"><span data-stu-id="d2274-119">**OldVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2274-120">Тип данных: **Win32 \_ классиккомкласс**</span><span class="sxs-lookup"><span data-stu-id="d2274-120">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="d2274-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d2274-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2274-122">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ классиккомкласс")</span><span class="sxs-lookup"><span data-stu-id="d2274-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="d2274-123">Ссылка на экземпляр, представляющий COM-компонент, который автоматически эмулируется другим компонентом.</span><span class="sxs-lookup"><span data-stu-id="d2274-123">Reference to the instance representing the COM component that is automatically emulated by another component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2274-124">Требования</span><span class="sxs-lookup"><span data-stu-id="d2274-124">Requirements</span></span>



| <span data-ttu-id="d2274-125">Требование</span><span class="sxs-lookup"><span data-stu-id="d2274-125">Requirement</span></span> | <span data-ttu-id="d2274-126">Значение</span><span class="sxs-lookup"><span data-stu-id="d2274-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2274-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d2274-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d2274-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2274-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d2274-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d2274-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d2274-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2274-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d2274-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d2274-131">Namespace</span></span><br/>                | <span data-ttu-id="d2274-132">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d2274-132">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d2274-133">MOF</span><span class="sxs-lookup"><span data-stu-id="d2274-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2274-134"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2274-134"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2274-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d2274-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2274-136"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2274-136"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2274-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2274-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="d2274-138">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d2274-138">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

