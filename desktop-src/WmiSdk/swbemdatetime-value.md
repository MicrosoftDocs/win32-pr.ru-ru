---
description: Возвращает или задает необработанную дату CIM в формате DMTF (распределенная задача управления принудительно).
ms.assetid: 426a60d5-c364-406e-8346-049a13d59c7f
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. Value (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Value
- ISWbemDateTime.Value
- ISWbemDateTime.get_Value
- ISWbemDateTime.put_Value
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2ecb3a42a865559ba9b3c3e5fbec7302f975fa0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155838"
---
# <a name="swbemdatetimevalue-property"></a><span data-ttu-id="b4b2c-103">SWbemDateTime. Value, свойство</span><span class="sxs-lookup"><span data-stu-id="b4b2c-103">SWbemDateTime.Value property</span></span>

<span data-ttu-id="b4b2c-104">Свойство **value** объекта [**SWbemDateTime**](swbemdatetime.md) Возвращает или задает необработанную дату CIM в формате DMTF (распределенная задача управления принудительно).</span><span class="sxs-lookup"><span data-stu-id="b4b2c-104">The **Value** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets the raw CIM date in the DMTF (Distributed Management Task Force) format.</span></span> <span data-ttu-id="b4b2c-105">Формат DMTF является строковым представлением значения [**DateTime**](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="b4b2c-105">The DMTF format is a string representation of the [**DATETIME**](datetime.md) value.</span></span> <span data-ttu-id="b4b2c-106">Это свойство является свойством по умолчанию для объектов **SWbemDateTime** .</span><span class="sxs-lookup"><span data-stu-id="b4b2c-106">This property is the default property for **SWbemDateTime** objects.</span></span> <span data-ttu-id="b4b2c-107">Свойство **value** имеет значение по умолчанию 00000101000000.000000 + 000.</span><span class="sxs-lookup"><span data-stu-id="b4b2c-107">The **Value** property has a default value of 00000101000000.000000+000.</span></span>

<span data-ttu-id="b4b2c-108">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b4b2c-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="b4b2c-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="b4b2c-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4b2c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4b2c-110">Syntax</span></span>


```VB
SWbemDateTime.Value As String
```



## <a name="property-value"></a><span data-ttu-id="b4b2c-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b4b2c-111">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="b4b2c-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b4b2c-112">Error codes</span></span>

<span data-ttu-id="b4b2c-113">После получения или задания свойства **value** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать приведенный ниже код ошибки.</span><span class="sxs-lookup"><span data-stu-id="b4b2c-113">After you get or set the **Value** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="b4b2c-114">**вбемерринвалидсинтакс** -2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="b4b2c-114">**wbemErrInvalidSyntax** - 2147749921 (0x80041021)</span></span>
</dt> <dd>

<span data-ttu-id="b4b2c-115">Недопустимый формат *strValue* .</span><span class="sxs-lookup"><span data-stu-id="b4b2c-115">The format of *strValue* is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="b4b2c-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="b4b2c-116">Examples</span></span>

<span data-ttu-id="b4b2c-117">Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="b4b2c-117">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="b4b2c-118">Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="b4b2c-118">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4b2c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b4b2c-119">Requirements</span></span>



| <span data-ttu-id="b4b2c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b4b2c-120">Requirement</span></span> | <span data-ttu-id="b4b2c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b4b2c-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4b2c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4b2c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b4b2c-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4b2c-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b4b2c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4b2c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b4b2c-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4b2c-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b4b2c-126">Header</span><span class="sxs-lookup"><span data-stu-id="b4b2c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4b2c-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4b2c-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4b2c-128">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="b4b2c-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="b4b2c-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b4b2c-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b4b2c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b4b2c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4b2c-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4b2c-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b4b2c-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="b4b2c-132">CLSID</span></span><br/>                    | <span data-ttu-id="b4b2c-133">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="b4b2c-133">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="b4b2c-134">IID</span><span class="sxs-lookup"><span data-stu-id="b4b2c-134">IID</span></span><br/>                      | <span data-ttu-id="b4b2c-135">IID \_ исвбемдатетиме</span><span class="sxs-lookup"><span data-stu-id="b4b2c-135">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="b4b2c-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4b2c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4b2c-137">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="b4b2c-137">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="b4b2c-138">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="b4b2c-138">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

