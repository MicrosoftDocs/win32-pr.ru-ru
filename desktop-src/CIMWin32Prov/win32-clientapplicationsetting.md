---
description: '\_Класс WMI взаимосвязей Win32 клиентаппликатионсеттинг связывает исполняемый файл и приложение модели COM, которое содержит параметры конфигурации COM для исполняемого файла.'
ms.assetid: c43d80ee-0f29-4452-b51f-f18543bc1d35
ms.tgt_platform: multiple
title: Класс Win32_ClientApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClientApplicationSetting
- Win32_ClientApplicationSetting.Application
- Win32_ClientApplicationSetting.Client
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fda1f1305904fa919bb2080fe5de02f0e5850a8a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990706"
---
# <a name="win32_clientapplicationsetting-class"></a><span data-ttu-id="899b2-103">\_Класс Win32 клиентаппликатионсеттинг</span><span class="sxs-lookup"><span data-stu-id="899b2-103">Win32\_ClientApplicationSetting class</span></span>

<span data-ttu-id="899b2-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ клиентаппликатионсеттинг** связывает исполняемый файл и приложение модели COM, которое содержит параметры конфигурации COM для исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="899b2-104">The **Win32\_ClientApplicationSetting** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates an executable file and a Component Object Model (COM) application that contains the COM configuration options for the executable file.</span></span>

<span data-ttu-id="899b2-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="899b2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="899b2-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="899b2-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="899b2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="899b2-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5E-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClientApplicationSetting
{
  Win32_DCOMApplication REF Application;
  CIM_DataFile          REF Client;
};
```

## <a name="members"></a><span data-ttu-id="899b2-108">Члены</span><span class="sxs-lookup"><span data-stu-id="899b2-108">Members</span></span>

<span data-ttu-id="899b2-109">Класс **Win32 \_ клиентаппликатионсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="899b2-109">The **Win32\_ClientApplicationSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="899b2-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="899b2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="899b2-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="899b2-111">Properties</span></span>

<span data-ttu-id="899b2-112">Класс **Win32 \_ клиентаппликатионсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="899b2-112">The **Win32\_ClientApplicationSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="899b2-113">**Приложение**</span><span class="sxs-lookup"><span data-stu-id="899b2-113">**Application**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="899b2-114">Тип данных: **Win32 \_ дкомаппликатион**</span><span class="sxs-lookup"><span data-stu-id="899b2-114">Data type: **Win32\_DCOMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="899b2-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="899b2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="899b2-116">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ дкомаппликатион")</span><span class="sxs-lookup"><span data-stu-id="899b2-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="899b2-117">Ссылка на экземпляр, представляющий COM-приложение, которое содержит параметры конфигурации исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="899b2-117">Reference to the instance that represents the COM application that contains configuration options of the executable file.</span></span>

</dd> <dt>

<span data-ttu-id="899b2-118">**Клиент**</span><span class="sxs-lookup"><span data-stu-id="899b2-118">**Client**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="899b2-119">Тип данных: **CIM \_ File**</span><span class="sxs-lookup"><span data-stu-id="899b2-119">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="899b2-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="899b2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="899b2-121">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ File")</span><span class="sxs-lookup"><span data-stu-id="899b2-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_DataFile")</span></span>
</dt> </dl>

<span data-ttu-id="899b2-122">Ссылка на экземпляр, представляющий исполняемый файл, использующий параметры COM.</span><span class="sxs-lookup"><span data-stu-id="899b2-122">Reference to the instance that represents the executable file that uses COM settings.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="899b2-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="899b2-123">Remarks</span></span>

<span data-ttu-id="899b2-124">**Win32 \_ Клиентаппликатионсеттинг** не поддерживает перечисление.</span><span class="sxs-lookup"><span data-stu-id="899b2-124">**Win32\_ClientApplicationSetting** does not support enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="899b2-125">Требования</span><span class="sxs-lookup"><span data-stu-id="899b2-125">Requirements</span></span>



| <span data-ttu-id="899b2-126">Требование</span><span class="sxs-lookup"><span data-stu-id="899b2-126">Requirement</span></span> | <span data-ttu-id="899b2-127">Значение</span><span class="sxs-lookup"><span data-stu-id="899b2-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="899b2-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="899b2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="899b2-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="899b2-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="899b2-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="899b2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="899b2-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="899b2-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="899b2-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="899b2-132">Namespace</span></span><br/>                | <span data-ttu-id="899b2-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="899b2-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="899b2-134">MOF</span><span class="sxs-lookup"><span data-stu-id="899b2-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="899b2-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="899b2-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="899b2-136">DLL</span><span class="sxs-lookup"><span data-stu-id="899b2-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="899b2-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="899b2-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="899b2-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="899b2-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="899b2-139">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="899b2-139">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

