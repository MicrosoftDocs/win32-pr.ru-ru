---
description: Метод Сетстреам объекта Record копирует содержимое указанного файла в указанное поле записи в виде потоковых данных. Данные потока не могут быть вставлены во временные поля.
ms.assetid: feb79371-d0c4-4bb0-b539-2f431ee1051b
title: Метод Record. Сетстреам
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.SetStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 94ec3d63b3dcd75a13c2c0ff62b624b89979d641
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679576"
---
# <a name="recordsetstream-method"></a><span data-ttu-id="bc8d8-104">Метод Record. Сетстреам</span><span class="sxs-lookup"><span data-stu-id="bc8d8-104">Record.SetStream method</span></span>

<span data-ttu-id="bc8d8-105">Метод **сетстреам** объекта [**Record**](record-object.md) копирует содержимое указанного файла в указанное поле записи в виде потоковых данных.</span><span class="sxs-lookup"><span data-stu-id="bc8d8-105">The **SetStream** method of the [**Record**](record-object.md) object copies the content of the specified file into the designated record field as stream data.</span></span> <span data-ttu-id="bc8d8-106">Данные потока не могут быть вставлены во временные поля.</span><span class="sxs-lookup"><span data-stu-id="bc8d8-106">Stream data cannot be inserted into temporary fields.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc8d8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc8d8-107">Syntax</span></span>


```JScript
Record.SetStream(
  field,
  filePath
)
```



## <a name="parameters"></a><span data-ttu-id="bc8d8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc8d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc8d8-109">*полями*</span><span class="sxs-lookup"><span data-stu-id="bc8d8-109">*field*</span></span> 
</dt> <dd>

<span data-ttu-id="bc8d8-110">Обязательный номер поля значения в записи, 1.</span><span class="sxs-lookup"><span data-stu-id="bc8d8-110">Required field number of the value within the record, 1-based.</span></span>

</dd> <dt>

<span data-ttu-id="bc8d8-111">*Равно*</span><span class="sxs-lookup"><span data-stu-id="bc8d8-111">*filePath*</span></span> 
</dt> <dd>

<span data-ttu-id="bc8d8-112">Расположение копируемого файла.</span><span class="sxs-lookup"><span data-stu-id="bc8d8-112">The location of the file to copy.</span></span> <span data-ttu-id="bc8d8-113">Перевод какого-либо типа не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bc8d8-113">No translation of any type is performed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc8d8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc8d8-114">Return value</span></span>

<span data-ttu-id="bc8d8-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bc8d8-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc8d8-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bc8d8-116">Remarks</span></span>

<span data-ttu-id="bc8d8-117">В случае сбоя метода можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="bc8d8-117">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc8d8-118">Требования</span><span class="sxs-lookup"><span data-stu-id="bc8d8-118">Requirements</span></span>



| <span data-ttu-id="bc8d8-119">Требование</span><span class="sxs-lookup"><span data-stu-id="bc8d8-119">Requirement</span></span> | <span data-ttu-id="bc8d8-120">Значение</span><span class="sxs-lookup"><span data-stu-id="bc8d8-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc8d8-121">Версия</span><span class="sxs-lookup"><span data-stu-id="bc8d8-121">Version</span></span><br/> | <span data-ttu-id="bc8d8-122">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bc8d8-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bc8d8-123">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bc8d8-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bc8d8-124">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="bc8d8-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="bc8d8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bc8d8-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="bc8d8-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc8d8-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="bc8d8-127">IID</span><span class="sxs-lookup"><span data-stu-id="bc8d8-127">IID</span></span><br/>     | <span data-ttu-id="bc8d8-128">IID \_ ирекорд определен как 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="bc8d8-128">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




