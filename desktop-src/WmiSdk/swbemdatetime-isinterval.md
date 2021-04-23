---
description: Логическое значение, указывающее, следует ли интерпретировать любое поле в значении DateTime CIM как интервал.
ms.assetid: ba5fcf17-7c26-4960-9da9-e380d90e5f3e
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. Wbemdisp (. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.IsInterval
- ISWbemDateTime.IsInterval
- ISWbemDateTime.get_IsInterval
- ISWbemDateTime.put_IsInterval
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 468ea16de4f1206a9a15c58c2c7891df8afd4c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272750"
---
# <a name="swbemdatetimeisinterval-property"></a><span data-ttu-id="f6b9a-103">SWbemDateTime. значение свойства интервала</span><span class="sxs-lookup"><span data-stu-id="f6b9a-103">SWbemDateTime.IsInterval property</span></span>

<span data-ttu-id="f6b9a-104">Свойство "значение **интервала** " объекта [**SWbemDateTime**](swbemdatetime.md) является логическим значением, указывающим, следует ли интерпретировать любое поле в значении DateTime CIM как интервал.</span><span class="sxs-lookup"><span data-stu-id="f6b9a-104">The **IsInterval** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether any field in a CIM datetime value should be interpreted as an interval.</span></span>

<span data-ttu-id="f6b9a-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f6b9a-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="f6b9a-106">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f6b9a-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6b9a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6b9a-107">Syntax</span></span>


```VB
SWbemDateTime.IsInterval As boolean
```



## <a name="property-value"></a><span data-ttu-id="f6b9a-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f6b9a-108">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="f6b9a-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="f6b9a-109">Examples</span></span>

<span data-ttu-id="f6b9a-110">Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений DateTime CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="f6b9a-110">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM datetime values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="f6b9a-111">Описание формата DateTime в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="f6b9a-111">For a description of the CIM datetime format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6b9a-112">Требования</span><span class="sxs-lookup"><span data-stu-id="f6b9a-112">Requirements</span></span>



| <span data-ttu-id="f6b9a-113">Требование</span><span class="sxs-lookup"><span data-stu-id="f6b9a-113">Requirement</span></span> | <span data-ttu-id="f6b9a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f6b9a-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6b9a-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6b9a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f6b9a-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6b9a-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f6b9a-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6b9a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f6b9a-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6b9a-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f6b9a-119">Header</span><span class="sxs-lookup"><span data-stu-id="f6b9a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6b9a-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6b9a-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f6b9a-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="f6b9a-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="f6b9a-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f6b9a-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f6b9a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f6b9a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6b9a-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6b9a-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f6b9a-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="f6b9a-125">CLSID</span></span><br/>                    | <span data-ttu-id="f6b9a-126">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="f6b9a-126">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="f6b9a-127">IID</span><span class="sxs-lookup"><span data-stu-id="f6b9a-127">IID</span></span><br/>                      | <span data-ttu-id="f6b9a-128">IID \_ исвбемдатетиме</span><span class="sxs-lookup"><span data-stu-id="f6b9a-128">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="f6b9a-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6b9a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6b9a-130">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="f6b9a-130">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="f6b9a-131">Формат даты и времени</span><span class="sxs-lookup"><span data-stu-id="f6b9a-131">Date and Time Format</span></span>](date-and-time-format.md)
</dt> </dl>

 

 




