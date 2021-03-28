---
description: Родительский класс, от которого производятся все классы трассировки системных событий. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 27979d9c-eca7-426f-8f8e-99443e5a0188
title: Класс MSNT_SystemTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSNT_SystemTrace
- MSNT_SystemTrace.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2eb0044029761a93a353a08a955d39d76c267f9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984569"
---
# <a name="msnt_systemtrace-class"></a><span data-ttu-id="2e1fd-104">\_Класс МСНТ системтраце</span><span class="sxs-lookup"><span data-stu-id="2e1fd-104">MSNT\_SystemTrace class</span></span>

<span data-ttu-id="2e1fd-105">Родительский класс, от которого производятся все классы трассировки системных событий.</span><span class="sxs-lookup"><span data-stu-id="2e1fd-105">The parent class from which all system event trace classes are derived.</span></span>

<span data-ttu-id="2e1fd-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="2e1fd-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e1fd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e1fd-107">Syntax</span></span>

``` syntax
[Guid("{9e814aad-3204-11d2-9a82-006008a86939}")]
class MSNT_SystemTrace : EventTrace
{
  uint32 Flags;
};
```

## <a name="members"></a><span data-ttu-id="2e1fd-108">Участники</span><span class="sxs-lookup"><span data-stu-id="2e1fd-108">Members</span></span>

<span data-ttu-id="2e1fd-109">Класс **МСНТ \_ системтраце** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2e1fd-109">The **MSNT\_SystemTrace** class has these types of members:</span></span>

-   [<span data-ttu-id="2e1fd-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="2e1fd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2e1fd-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="2e1fd-111">Properties</span></span>

<span data-ttu-id="2e1fd-112">Класс **МСНТ \_ системтраце** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2e1fd-112">The **MSNT\_SystemTrace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e1fd-113">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="2e1fd-113">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e1fd-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e1fd-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e1fd-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2e1fd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e1fd-116">Квалификаторы: **дефиневалуес {" \_ \_ процесс флага трассировки событий", "поток флагов трассировки событий", "нагрузка изображения флага трассировки событий", " \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ счетчики процесса флага трассировки событий \_ ", "флаг трассировки событий \_ , \_ \_ \_ ксвитч", "флаг трассировки событий \_ \_ \_ DPC", " \_ \_ прерывание флага трассировки событий \_ ", " \_ флаг трассировки событий \_ \_ системкалл", " \_ флаг трассировки событий \_ \_ дисковые \_ операции ввода-вывода", " \_ флаг трассировки событий \_ \_ дисковые операции ввода-вывода", "флаг трассировки событий диск ввода-вывода", "Диспетчер флагов трассировки событий", "ошибки страниц памяти для флагов трассировки событий", "фиксированный размер памяти для флага трассировки событий", "состояние \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ виртуальной \_ \_ \_ \_ сети \_ tcpip" \_ \_ Реестр флагов трассировки событий \_ "," \_ флаг трассировки событий \_ \_ ALPC "," предельное разбиение флага трассировки событий "," драйвер флага трассировки событий "," профиль флага трассировки событий "," Трассировка события — \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ файл \_ операций ввода-вывода "," \_ Отслеживание событий Flag- \_ \_ File \_ IO \_ init "}**, **ValueMap {" 0x00000001 "," 0x00000002 "," 0x00000004 "," 0x00000008 "," 0x00000010 "," 0x00000020 "," 0x00000040 "," 0x00000080 "," 0x00000100 " , "0x00000200", "0x00000400", "0x00000800", "0x00001000", "0x00002000", "0x00004000", "0x00010000", "0x00020000", "0x00100000", "0x00200000", "0x00800000", "0x01000000", "** 0x02000000", "0x04000000"}</span><span class="sxs-lookup"><span data-stu-id="2e1fd-116">Qualifiers: **DefineValues{"EVENT\_TRACE\_FLAG\_PROCESS", "EVENT\_TRACE\_FLAG\_THREAD", "EVENT\_TRACE\_FLAG\_IMAGE\_LOAD", "EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS", "EVENT\_TRACE\_FLAG\_CSWITCH", "EVENT\_TRACE\_FLAG\_DPC", "EVENT\_TRACE\_FLAG\_INTERRUPT", "EVENT\_TRACE\_FLAG\_SYSTEMCALL", "EVENT\_TRACE\_FLAG\_DISK\_IO", "EVENT\_TRACE\_FLAG\_DISK\_FILE\_IO", "EVENT\_TRACE\_FLAG\_DISK\_IO\_INIT", "EVENT\_TRACE\_FLAG\_DISPATCHER", "EVENT\_TRACE\_FLAG\_MEMORY\_PAGE\_FAULTS", "EVENT\_TRACE\_FLAG\_MEMORY\_HARD\_FAULTS", "EVENT\_TRACE\_FLAG\_VIRTUAL\_ALLOC", "EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP", "EVENT\_TRACE\_FLAG\_REGISTRY", "EVENT\_TRACE\_FLAG\_ALPC", "EVENT\_TRACE\_FLAG\_SPLIT\_IO", "EVENT\_TRACE\_FLAG\_DRIVER", "EVENT\_TRACE\_FLAG\_PROFILE", "EVENT\_TRACE\_FLAG\_FILE\_IO", "EVENT\_TRACE\_FLAG\_FILE\_IO\_INIT"}**, **ValueMap{"0x00000001", "0x00000002", "0x00000004", "0x00000008", "0x00000010", "0x00000020", "0x00000040", "0x00000080", "0x00000100", "0x00000200", "0x00000400", "0x00000800", "0x00001000", "0x00002000", "0x00004000", "0x00010000", "0x00020000", "0x00100000", "0x00200000", "0x00800000", "0x01000000", "0x02000000", "0x04000000"}**</span></span>
</dt> </dl>

<span data-ttu-id="2e1fd-117">Включить флаг, указывающий включенных поставщиков ядер.</span><span class="sxs-lookup"><span data-stu-id="2e1fd-117">Enable flag that indicates the enabled kernel providers.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e1fd-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2e1fd-118">Requirements</span></span>



| <span data-ttu-id="2e1fd-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2e1fd-119">Requirement</span></span> | <span data-ttu-id="2e1fd-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2e1fd-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2e1fd-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e1fd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2e1fd-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2e1fd-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2e1fd-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e1fd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2e1fd-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2e1fd-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



 

 




