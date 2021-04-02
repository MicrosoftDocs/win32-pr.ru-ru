---
description: Абстрактный базовый класс, из которого производятся все классы данных поставщика (MCA), например Мсмкаинфо \_ равмкадата. Этот класс доступен только в 64-разрядных системах Windows.
ms.assetid: 22ec8343-fc4f-4b14-9354-26b5d6a6fe09
title: Класс Мсмкаинфо
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 31fc35b1d680d900af929ea8a828bcb23d222f66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072734"
---
# <a name="msmcainfo-class"></a><span data-ttu-id="f276e-104">Класс Мсмкаинфо</span><span class="sxs-lookup"><span data-stu-id="f276e-104">MSMCAInfo class</span></span>

<span data-ttu-id="f276e-105">Класс **мсмкаинфо** является абстрактным базовым классом, из которого производятся все классы данных поставщика (например, [**мсмкаинфо \_ равмкадата**](msmcainfo-rawmcadata.md)).</span><span class="sxs-lookup"><span data-stu-id="f276e-105">The **MSMCAInfo** class is an abstract base class from which all Machine Check Architecture (MCA) provider data classes, such as [**MSMCAInfo\_RawMCAData**](msmcainfo-rawmcadata.md), are derived.</span></span> <span data-ttu-id="f276e-106">Поставщик MCA также имеет классы событий, производные от [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="f276e-106">The MCA provider also has event classes, derived from [**WMIEvent**](wmievent.md).</span></span> <span data-ttu-id="f276e-107">Этот класс доступен только в 64-разрядных системах Windows.</span><span class="sxs-lookup"><span data-stu-id="f276e-107">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="f276e-108">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f276e-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f276e-109">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="f276e-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f276e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f276e-110">Syntax</span></span>

``` syntax
class MSMCAInfo
{
};
```

## <a name="members"></a><span data-ttu-id="f276e-111">Члены</span><span class="sxs-lookup"><span data-stu-id="f276e-111">Members</span></span>

<span data-ttu-id="f276e-112">Класс **мсмкаинфо** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="f276e-112">The **MSMCAInfo** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="f276e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f276e-113">Requirements</span></span>



| <span data-ttu-id="f276e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f276e-114">Requirement</span></span> | <span data-ttu-id="f276e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f276e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f276e-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f276e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f276e-117">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f276e-117">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="f276e-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f276e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f276e-119">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f276e-119">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="f276e-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f276e-120">Namespace</span></span><br/>                | <span data-ttu-id="f276e-121">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="f276e-121">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="f276e-122">MOF</span><span class="sxs-lookup"><span data-stu-id="f276e-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f276e-123"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f276e-123"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="f276e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f276e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f276e-125"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f276e-125"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f276e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f276e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f276e-127">Классы МСМКА</span><span class="sxs-lookup"><span data-stu-id="f276e-127">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="f276e-128">**\_Заголовок мсмкаевент**</span><span class="sxs-lookup"><span data-stu-id="f276e-128">**MSMCAEvent\_Header**</span></span>](msmcaevent-header.md)
</dt> <dt>

[<span data-ttu-id="f276e-129">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="f276e-129">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

 




