---
description: 'Оператор вычитания класса Вбемтиме (&\# 8211;) был перегружен в:'
audience: developer
ms.assetid: 0fa51aab-7ea2-4af7-bb12-1646388b0405
ms.tgt_platform: multiple
title: 'Операторы Вбемтиме:: operator-(Вбемтиме. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 39256ba9d922ea9d3eef8e442115e840b963ca71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713026"
---
# <a name="wbemtimeoperator--operators"></a><span data-ttu-id="2c5e8-103">Операторы Вбемтиме:: operator-</span><span class="sxs-lookup"><span data-stu-id="2c5e8-103">WBEMTime::operator- operators</span></span>

<span data-ttu-id="2c5e8-104">\[Класс [**вбемтиме**](wbemtime.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="2c5e8-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="2c5e8-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="2c5e8-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="2c5e8-106">Оператор вычитания класса [**вбемтиме**](wbemtime.md) () перегружен до:</span><span class="sxs-lookup"><span data-stu-id="2c5e8-106">The [**WBEMTime**](wbemtime.md) class subtraction operator (�) has been overloaded to:</span></span>

-   <span data-ttu-id="2c5e8-107">Вычитание интервала времени из времени объекта для создания нового объекта времени, содержащего результирующее время.</span><span class="sxs-lookup"><span data-stu-id="2c5e8-107">Subtract a time span from an object's time to produce a new time object that contains the resulting time.</span></span>
-   <span data-ttu-id="2c5e8-108">Вычтите время из времени объекта, чтобы создать новый объект интервала времени, содержащий разницу между двумя значениями времени.</span><span class="sxs-lookup"><span data-stu-id="2c5e8-108">Subtract a time from the object's time to produce a new time span object that contains the difference between the two times.</span></span>

### <a name="overload-list"></a><span data-ttu-id="2c5e8-109">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="2c5e8-109">Overload list</span></span>



| <span data-ttu-id="2c5e8-110">Оператор</span><span class="sxs-lookup"><span data-stu-id="2c5e8-110">Operator</span></span>                                                                         | <span data-ttu-id="2c5e8-111">Описание</span><span class="sxs-lookup"><span data-stu-id="2c5e8-111">Description</span></span>                                                                      |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="2c5e8-112">**operator — (Вбемтиме&)**</span><span class="sxs-lookup"><span data-stu-id="2c5e8-112">**operator-(WBEMTime&)**</span></span>](/windows/win32/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize)         | <span data-ttu-id="2c5e8-113">Вычитает **вбемтиме** из **вбемтиме**.</span><span class="sxs-lookup"><span data-stu-id="2c5e8-113">Subtracts a **WBEMTime** from a **WBEMTime**.</span></span><br/>                         |
| <span data-ttu-id="2c5e8-114">[**operator — (Вбемтимеспан&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_))</span><span class="sxs-lookup"><span data-stu-id="2c5e8-114">[**operator-(WBEMTimeSpan&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_))</span></span> | <span data-ttu-id="2c5e8-115">Вычитает [**вбемтимеспан**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) из **вбемтиме**.</span><span class="sxs-lookup"><span data-stu-id="2c5e8-115">Subtracts a [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) from a **WBEMTime**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2c5e8-116">Требования</span><span class="sxs-lookup"><span data-stu-id="2c5e8-116">Requirements</span></span>



| <span data-ttu-id="2c5e8-117">Требование</span><span class="sxs-lookup"><span data-stu-id="2c5e8-117">Requirement</span></span> | <span data-ttu-id="2c5e8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2c5e8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c5e8-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c5e8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2c5e8-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c5e8-120">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="2c5e8-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c5e8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2c5e8-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c5e8-122">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="2c5e8-123">Header</span><span class="sxs-lookup"><span data-stu-id="2c5e8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c5e8-124"><dt>Вбемтиме. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c5e8-124"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="2c5e8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2c5e8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c5e8-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c5e8-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="2c5e8-127">�</span><span class="sxs-lookup"><span data-stu-id="2c5e8-127">�</span></span>

<span data-ttu-id="2c5e8-128">�</span><span class="sxs-lookup"><span data-stu-id="2c5e8-128">�</span></span>
