---
description: Метод Реадстреам объекта Record считывает указанное число байтов из поля записи, содержащего потоковые данные.
ms.assetid: 845e23e5-6379-4592-aee4-cd6832baf335
title: Метод Record. Реадстреам
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.ReadStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bc77e07231d086f15086662d60581d4c5992bf5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668636"
---
# <a name="recordreadstream-method"></a><span data-ttu-id="dc24d-103">Метод Record. Реадстреам</span><span class="sxs-lookup"><span data-stu-id="dc24d-103">Record.ReadStream method</span></span>

<span data-ttu-id="dc24d-104">Метод **реадстреам** объекта [**Record**](record-object.md) считывает указанное число байтов из поля записи, содержащего потоковые данные.</span><span class="sxs-lookup"><span data-stu-id="dc24d-104">The **ReadStream** method of the [**Record**](record-object.md) object reads a specified number of bytes from a record field that contains stream data.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc24d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc24d-105">Syntax</span></span>


```JScript
Record.ReadStream(
  field,
  length,
  format
)
```



## <a name="parameters"></a><span data-ttu-id="dc24d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc24d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc24d-107">*полями*</span><span class="sxs-lookup"><span data-stu-id="dc24d-107">*field*</span></span> 
</dt> <dd>

<span data-ttu-id="dc24d-108">Номер поля, требуемого для значения в записи, 1.</span><span class="sxs-lookup"><span data-stu-id="dc24d-108">The required field number of the value within the record, 1-based.</span></span>

</dd> <dt>

<span data-ttu-id="dc24d-109">*length*</span><span class="sxs-lookup"><span data-stu-id="dc24d-109">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="dc24d-110">Требуемое число байтов для чтения из потока.</span><span class="sxs-lookup"><span data-stu-id="dc24d-110">The required number of bytes to read from the stream.</span></span>

</dd> <dt>

<span data-ttu-id="dc24d-111">*format*</span><span class="sxs-lookup"><span data-stu-id="dc24d-111">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="dc24d-112">Требуется интерпретация и возвращение байтов данных.</span><span class="sxs-lookup"><span data-stu-id="dc24d-112">Required interpretation and return of the data bytes.</span></span>



| <span data-ttu-id="dc24d-113">Имя параметра</span><span class="sxs-lookup"><span data-stu-id="dc24d-113">Parameter name</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="dc24d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="dc24d-114">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="msiReadStreamInteger"></span><span id="msireadstreaminteger"></span><span id="MSIREADSTREAMINTEGER"></span><dl> <span data-ttu-id="dc24d-115"><dt>**мсиреадстреаминтежер**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dc24d-115"><dt>**msiReadStreamInteger**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="dc24d-116">В виде длинного целого числа длина должна быть от 1 до 4.</span><span class="sxs-lookup"><span data-stu-id="dc24d-116">As a long integer the length must be 1 to 4.</span></span><br/>             |
| <span id="msiReadStreamBytes"></span><span id="msireadstreambytes"></span><span id="MSIREADSTREAMBYTES"></span><dl> <span data-ttu-id="dc24d-117"><dt>**мсиреадстреамбитес**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="dc24d-117"><dt>**msiReadStreamBytes**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="dc24d-118">Данные в виде **BSTR**— один байт на символ.</span><span class="sxs-lookup"><span data-stu-id="dc24d-118">The data as a **BSTR**—one byte per character.</span></span><br/>           |
| <span id="msiReadStreamAnsi"></span><span id="msireadstreamansi"></span><span id="MSIREADSTREAMANSI"></span><dl> <span data-ttu-id="dc24d-119"><dt>**мсиреадстреаманси**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="dc24d-119"><dt>**msiReadStreamAnsi**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="dc24d-120">Байты ANSI, переведенные в Юникод **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="dc24d-120">The ANSI bytes translated to a Unicode **BSTR**.</span></span><br/>         |
| <span id="msiReadStreamDirect"></span><span id="msireadstreamdirect"></span><span id="MSIREADSTREAMDIRECT"></span><dl> <span data-ttu-id="dc24d-121"><dt>**мсиреадстреамдирект**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="dc24d-121"><dt>**msiReadStreamDirect**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="dc24d-122">Пары байтов, возвращаемые непосредственно в виде **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="dc24d-122">The byte pairs that are returned directly as a **BSTR**.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc24d-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc24d-123">Return value</span></span>

<span data-ttu-id="dc24d-124">Этот метод возвращает строку, содержащую запрошенное число байтов, считанных из поля записи.</span><span class="sxs-lookup"><span data-stu-id="dc24d-124">This method returns a string that contains the requested number of bytes read from a record field.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc24d-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc24d-125">Remarks</span></span>

<span data-ttu-id="dc24d-126">Возвращенное значение несуществующего поля является пустым значением.</span><span class="sxs-lookup"><span data-stu-id="dc24d-126">The returned value of a nonexistent field is an Empty value.</span></span> <span data-ttu-id="dc24d-127">Если в потоке меньше байтов, запрошенных счетчиком, возвращаемая строка сокращается соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="dc24d-127">If the stream has fewer bytes that the count requested, the returned string is shortened appropriately.</span></span>

<span data-ttu-id="dc24d-128">Пример этого метода см. [в разделе Копирование файла ANSI в поле базы данных](copy-ansi-file-into-a-database-field.md).</span><span class="sxs-lookup"><span data-stu-id="dc24d-128">For an example of this method, see [Copy ANSI File Into a Database Field](copy-ansi-file-into-a-database-field.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc24d-129">Требования</span><span class="sxs-lookup"><span data-stu-id="dc24d-129">Requirements</span></span>



| <span data-ttu-id="dc24d-130">Требование</span><span class="sxs-lookup"><span data-stu-id="dc24d-130">Requirement</span></span> | <span data-ttu-id="dc24d-131">Значение</span><span class="sxs-lookup"><span data-stu-id="dc24d-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc24d-132">Версия</span><span class="sxs-lookup"><span data-stu-id="dc24d-132">Version</span></span><br/> | <span data-ttu-id="dc24d-133">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dc24d-133">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dc24d-134">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dc24d-134">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dc24d-135">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc24d-135">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="dc24d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="dc24d-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="dc24d-137"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc24d-137"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="dc24d-138">IID</span><span class="sxs-lookup"><span data-stu-id="dc24d-138">IID</span></span><br/>     | <span data-ttu-id="dc24d-139">IID \_ ирекорд определен как 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="dc24d-139">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




