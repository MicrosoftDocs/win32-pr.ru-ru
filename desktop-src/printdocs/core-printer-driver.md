---
description: Представляет драйвер принтера, от которого зависят другие драйверы принтеров.
ms.assetid: b03f9ac1-7ad2-4aee-b496-e1ee15ba7d38
title: Структура CORE_PRINTER_DRIVER (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CORE_PRINTER_DRIVER
- _CORE_PRINTER_DRIVERA
- _CORE_PRINTER_DRIVERW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 786fa3491919659fca60700cfb086023c3fdef3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647353"
---
# <a name="core_printer_driver-structure"></a><span data-ttu-id="74294-103">Основная \_ \_ Структура драйвера принтера</span><span class="sxs-lookup"><span data-stu-id="74294-103">CORE\_PRINTER\_DRIVER structure</span></span>

<span data-ttu-id="74294-104">Представляет драйвер принтера, от которого зависят другие драйверы принтеров.</span><span class="sxs-lookup"><span data-stu-id="74294-104">Represents a printer driver on which other printer drivers depend.</span></span>

## <a name="syntax"></a><span data-ttu-id="74294-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74294-105">Syntax</span></span>


```C++
typedef struct _CORE_PRINTER_DRIVER {
  GUID      CoreDriverGUID;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  TCHAR     szPackageID[MAX_PATH];
} CORE_PRINTER_DRIVER, *PCORE_PRINTER_DRIVER;
```



## <a name="members"></a><span data-ttu-id="74294-106">Члены</span><span class="sxs-lookup"><span data-stu-id="74294-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="74294-107">**коредривергуид**</span><span class="sxs-lookup"><span data-stu-id="74294-107">**CoreDriverGUID**</span></span>
</dt> <dd>

<span data-ttu-id="74294-108">Идентификатор GUID основного драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="74294-108">The GUID of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="74294-109">**фтдривердате**</span><span class="sxs-lookup"><span data-stu-id="74294-109">**ftDriverDate**</span></span>
</dt> <dd>

<span data-ttu-id="74294-110">Дата и время последней версии драйвера основного принтера.</span><span class="sxs-lookup"><span data-stu-id="74294-110">The date and time of the latest version of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="74294-111">**двлдриверверсион**</span><span class="sxs-lookup"><span data-stu-id="74294-111">**dwlDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="74294-112">Идентификатор версии последней версии драйвера основного принтера.</span><span class="sxs-lookup"><span data-stu-id="74294-112">The version ID of the latest version of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="74294-113">**Сзпаккажеид \[ максимальный \_ путь\]**</span><span class="sxs-lookup"><span data-stu-id="74294-113">**szPackageID\[MAX\_PATH\]**</span></span>
</dt> <dd>

<span data-ttu-id="74294-114">Путь к пакету драйверов, который содержит основной драйвер принтера.</span><span class="sxs-lookup"><span data-stu-id="74294-114">The path to the driver package that contains the core printer driver.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74294-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74294-115">Remarks</span></span>

<span data-ttu-id="74294-116">Эта структура может представлять базовый драйвер производителя, от которого зависят драйверы различных моделей принтеров.</span><span class="sxs-lookup"><span data-stu-id="74294-116">This structure can represent a manufacturer's base driver on which the drivers for various printer models are dependent.</span></span>

## <a name="requirements"></a><span data-ttu-id="74294-117">Требования</span><span class="sxs-lookup"><span data-stu-id="74294-117">Requirements</span></span>



| <span data-ttu-id="74294-118">Требование</span><span class="sxs-lookup"><span data-stu-id="74294-118">Requirement</span></span> | <span data-ttu-id="74294-119">Значение</span><span class="sxs-lookup"><span data-stu-id="74294-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74294-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74294-120">Minimum supported client</span></span><br/> | <span data-ttu-id="74294-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="74294-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="74294-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74294-122">Minimum supported server</span></span><br/> | <span data-ttu-id="74294-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="74294-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="74294-124">Header</span><span class="sxs-lookup"><span data-stu-id="74294-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="74294-125"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74294-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="74294-126">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="74294-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="74294-127">**\_ Основной \_ принтер \_ дриверв** (Юникод) и **\_ основной \_ \_ драйвер принтера** a (ANSI)</span><span class="sxs-lookup"><span data-stu-id="74294-127">**\_CORE\_PRINTER\_DRIVERW** (Unicode) and **\_CORE\_PRINTER\_DRIVERA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="74294-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74294-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74294-129">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="74294-129">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="74294-130">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="74294-130">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




