---
description: Функция Модифифраме изменяет существующий кадр на новые данные.
ms.assetid: ebd248e4-b248-4f4a-8b94-a6d1c331d12a
title: Функция Модифифраме (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ModifyFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: af3ef6c2c5ccae2b6410ac8fc81c815f790b17a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662449"
---
# <a name="modifyframe-function"></a><span data-ttu-id="26d47-103">Функция Модифифраме</span><span class="sxs-lookup"><span data-stu-id="26d47-103">ModifyFrame function</span></span>

<span data-ttu-id="26d47-104">Функция **модифифраме** изменяет существующий кадр на новые данные.</span><span class="sxs-lookup"><span data-stu-id="26d47-104">The **ModifyFrame** function alters an existing frame with new data.</span></span>

## <a name="syntax"></a><span data-ttu-id="26d47-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26d47-105">Syntax</span></span>


```C++
HFRAME WINAPI ModifyFrame(
  _In_  HCAPTURE hCapture,
  _In_  DWORD    FrameNumber,
  _In_  LPBYTE   FrameData,
  _In_  DWORD    FrameLength,
  _Out_ __int64  TimeStamp
);
```



## <a name="parameters"></a><span data-ttu-id="26d47-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="26d47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26d47-107">*хкаптуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="26d47-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26d47-108">Обработчик для записи.</span><span class="sxs-lookup"><span data-stu-id="26d47-108">Handle to the capture.</span></span> <span data-ttu-id="26d47-109">Дополнительные сведения о получении маркера записи см. в подразделе "Примечания" этой статьи **модифифраме** .</span><span class="sxs-lookup"><span data-stu-id="26d47-109">For information about obtaining the capture handle, see the Remarks section of this **ModifyFrame** topic.</span></span>

</dd> <dt>

<span data-ttu-id="26d47-110">*Фраменумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="26d47-110">*FrameNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26d47-111">Номер индекса кадра.</span><span class="sxs-lookup"><span data-stu-id="26d47-111">Frame index number.</span></span>

</dd> <dt>

<span data-ttu-id="26d47-112">*Фрамедата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="26d47-112">*FrameData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26d47-113">Указатель на массив байтов, содержащий новые данные кадра.</span><span class="sxs-lookup"><span data-stu-id="26d47-113">Pointer to an array of bytes that contain the new frame data.</span></span>

</dd> <dt>

<span data-ttu-id="26d47-114">*Фрамеленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="26d47-114">*FrameLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26d47-115">Длина новых данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="26d47-115">Length of the new data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="26d47-116">*Метка времени* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="26d47-116">*TimeStamp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26d47-117">Метка времени, указывающая, когда был изменен кадр.</span><span class="sxs-lookup"><span data-stu-id="26d47-117">Time stamp indicating when the frame was modified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26d47-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26d47-118">Return value</span></span>

<span data-ttu-id="26d47-119">Если функция выполнена успешно, возвращаемое значение является маркером нового кадра.</span><span class="sxs-lookup"><span data-stu-id="26d47-119">If the function is successful, the return value is a handle to a new frame.</span></span>

<span data-ttu-id="26d47-120">Если функция завершилась неудачно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="26d47-120">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="26d47-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26d47-121">Remarks</span></span>

<span data-ttu-id="26d47-122">Если вызов выполнен успешно, функция **модифифраме** уничтожает исходный кадр.</span><span class="sxs-lookup"><span data-stu-id="26d47-122">If the call is successful, the **ModifyFrame** function destroys the original frame.</span></span>

<span data-ttu-id="26d47-123">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **модифифраме** .</span><span class="sxs-lookup"><span data-stu-id="26d47-123">[*Experts*](e.md) and [*parsers*](p.md) can call the **ModifyFrame** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="26d47-124">Требования</span><span class="sxs-lookup"><span data-stu-id="26d47-124">Requirements</span></span>



| <span data-ttu-id="26d47-125">Требование</span><span class="sxs-lookup"><span data-stu-id="26d47-125">Requirement</span></span> | <span data-ttu-id="26d47-126">Значение</span><span class="sxs-lookup"><span data-stu-id="26d47-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="26d47-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26d47-127">Minimum supported client</span></span><br/> | <span data-ttu-id="26d47-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="26d47-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="26d47-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26d47-129">Minimum supported server</span></span><br/> | <span data-ttu-id="26d47-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="26d47-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="26d47-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="26d47-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="26d47-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="26d47-132"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="26d47-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="26d47-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="26d47-134"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26d47-134"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="26d47-135">DLL</span><span class="sxs-lookup"><span data-stu-id="26d47-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26d47-136"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26d47-136"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




