---
description: Функция Жеткаптуремактипе Возвращает тип MAC для данной записи.
ms.assetid: de0dfb36-df3a-4f6e-b266-09c81dfdc88b
title: Функция Жеткаптуремактипе (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 73569109db5b958e854135461a0e480178d0105a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808722"
---
# <a name="getcapturemactype-function"></a><span data-ttu-id="971b6-103">Функция Жеткаптуремактипе</span><span class="sxs-lookup"><span data-stu-id="971b6-103">GetCaptureMacType function</span></span>

<span data-ttu-id="971b6-104">Функция **жеткаптуремактипе** ВОЗВРАЩАЕТ тип Mac для данной записи.</span><span class="sxs-lookup"><span data-stu-id="971b6-104">The **GetCaptureMacType** function returns the MAC type of a given capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="971b6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="971b6-105">Syntax</span></span>


```C++
DWORD WINAPI GetCaptureMacType(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="971b6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="971b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="971b6-107">*хкаптуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="971b6-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="971b6-108">Обработчик для записи.</span><span class="sxs-lookup"><span data-stu-id="971b6-108">Handle to the capture.</span></span> <span data-ttu-id="971b6-109">Дополнительные сведения о получении маркера записи см. в подразделе "Примечания" этого раздела **жеткаптуремактипе** .</span><span class="sxs-lookup"><span data-stu-id="971b6-109">For information about obtaining the capture handle, see the Remarks section in this **GetCaptureMacType** topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="971b6-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="971b6-110">Return value</span></span>

<span data-ttu-id="971b6-111">Если функция выполнена успешно, возвращаемое значение является одним из следующих типов MAC.</span><span class="sxs-lookup"><span data-stu-id="971b6-111">If the function is successful, the return value is one of the following MAC types.</span></span>

-   <span data-ttu-id="971b6-112">\_неизвестный тип Mac \_</span><span class="sxs-lookup"><span data-stu-id="971b6-112">MAC\_TYPE\_UNKNOWN</span></span>
-   <span data-ttu-id="971b6-113">\_тип Mac \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="971b6-113">MAC\_TYPE\_ETHERNET</span></span>
-   <span data-ttu-id="971b6-114">\_тип Mac \_ токенринг</span><span class="sxs-lookup"><span data-stu-id="971b6-114">MAC\_TYPE\_TOKENRING</span></span>
-   <span data-ttu-id="971b6-115">\_тип Mac \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="971b6-115">MAC\_TYPE\_FDDI</span></span>

<span data-ttu-id="971b6-116">Если функция завершается неудачно, возвращаемое значение является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="971b6-116">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="971b6-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="971b6-117">Return code</span></span>                                                                                              | <span data-ttu-id="971b6-118">Описание</span><span class="sxs-lookup"><span data-stu-id="971b6-118">Description</span></span>                                                 |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="971b6-119"><dt>**\_неизвестный тип Mac-адреса нмерр \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="971b6-119"><dt>**NMERR\_MAC\_TYPE\_UNKNOWN**</dt></span></span> </dl> | <span data-ttu-id="971b6-120">Сетевой монитор не удалось найти известный тип MAC.</span><span class="sxs-lookup"><span data-stu-id="971b6-120">Network Monitor could not find a known MAC type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="971b6-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="971b6-121">Remarks</span></span>

<span data-ttu-id="971b6-122">Маркер записи может быть получен несколькими способами в зависимости от того, кто выполняет вызов.</span><span class="sxs-lookup"><span data-stu-id="971b6-122">The handle of the capture can be obtained in several ways, depending on who makes the call.</span></span> <span data-ttu-id="971b6-123">Для экспертов этот маркер указывается в элементе **хкаптуре** структуры [експертстартупинфо](expertstartupinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="971b6-123">For experts, the handle is specified in the **hCapture** member of the [EXPERTSTARTUPINFO](expertstartupinfo.md) structure.</span></span> <span data-ttu-id="971b6-124">Для средств синтаксического анализа можно получить маркер записи, вызвав функцию [жетфрамекаптурехандле](getframecapturehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="971b6-124">For parsers, the capture handle can be obtained by calling the [GetFrameCaptureHandle](getframecapturehandle.md) function.</span></span>

<span data-ttu-id="971b6-125">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жеткаптуремактипе** .</span><span class="sxs-lookup"><span data-stu-id="971b6-125">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureMacType** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="971b6-126">Требования</span><span class="sxs-lookup"><span data-stu-id="971b6-126">Requirements</span></span>



| <span data-ttu-id="971b6-127">Требование</span><span class="sxs-lookup"><span data-stu-id="971b6-127">Requirement</span></span> | <span data-ttu-id="971b6-128">Значение</span><span class="sxs-lookup"><span data-stu-id="971b6-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="971b6-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="971b6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="971b6-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="971b6-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="971b6-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="971b6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="971b6-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="971b6-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="971b6-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="971b6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="971b6-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="971b6-134"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="971b6-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="971b6-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="971b6-136"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="971b6-136"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="971b6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="971b6-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="971b6-138"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="971b6-138"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




