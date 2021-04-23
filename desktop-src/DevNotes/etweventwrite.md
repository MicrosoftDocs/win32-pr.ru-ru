---
description: Дополнительные сведения о функции Етвевентврите
title: етвевентврите
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWrite
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 149f611dfb298749befca805509e05fa2dec497a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072496"
---
# <a name="etweventwrite-function"></a><span data-ttu-id="89d3d-103">Функция Етвевентврите</span><span class="sxs-lookup"><span data-stu-id="89d3d-103">EtwEventWrite function</span></span>

<span data-ttu-id="89d3d-104">[Функция Етвевентврите и возвращаемые ею структуры являются внутренними по отношению к операционной системе и могут быть изменены с одного выпуска Windows на другой.]</span><span class="sxs-lookup"><span data-stu-id="89d3d-104">[The EtwEventWrite function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.]</span></span>

<span data-ttu-id="89d3d-105">Записывает базовое событие в сеанс.</span><span class="sxs-lookup"><span data-stu-id="89d3d-105">Writes a basic event to a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="89d3d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89d3d-106">Syntax</span></span>

```C++
ULONG 
EVNTAPI
EtwEventWrite(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in ULONG UserDataCount,
    __in_ecount_opt(UserDataCount) PEVENT_DATA_DESCRIPTOR UserData
    );
```

## <a name="parameters"></a><span data-ttu-id="89d3d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="89d3d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89d3d-108">*регхандле*</span><span class="sxs-lookup"><span data-stu-id="89d3d-108">*RegHandle*</span></span>
</dt> <dd>

<span data-ttu-id="89d3d-109">Регхандле для поставщика.</span><span class="sxs-lookup"><span data-stu-id="89d3d-109">RegHandle for the provider.</span></span>

</dd> <dt>

<span data-ttu-id="89d3d-110">*EventDescriptor*</span><span class="sxs-lookup"><span data-stu-id="89d3d-110">*EventDescriptor*</span></span>
</dt> <dd>

<span data-ttu-id="89d3d-111">Дескриптор события для записи в журнал.</span><span class="sxs-lookup"><span data-stu-id="89d3d-111">Event descriptor of the event to log.</span></span>

</dd> <dt>

<span data-ttu-id="89d3d-112">*усердатакаунт*</span><span class="sxs-lookup"><span data-stu-id="89d3d-112">*UserDataCount*</span></span>
</dt> <dd>

<span data-ttu-id="89d3d-113">Число элементов данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="89d3d-113">Number of user data items.</span></span>

</dd> <dt>

<span data-ttu-id="89d3d-114">*UserData*</span><span class="sxs-lookup"><span data-stu-id="89d3d-114">*UserData*</span></span>
</dt> <dd>

<span data-ttu-id="89d3d-115">Указатель на массив элементов данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="89d3d-115">Pointer to an array of user data items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89d3d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89d3d-116">Return value</span></span>

<span data-ttu-id="89d3d-117">Код ошибки Win32.</span><span class="sxs-lookup"><span data-stu-id="89d3d-117">A Win32 error code.</span></span>


## <a name="remarks"></a><span data-ttu-id="89d3d-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89d3d-118">Remarks</span></span>

<span data-ttu-id="89d3d-119">Функция Етвевентврите и возвращаемые ею структуры являются внутренними по отношению к операционной системе и могут изменяться от одного выпуска Windows к другому.</span><span class="sxs-lookup"><span data-stu-id="89d3d-119">The EtwEventWrite function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="89d3d-120">Чтобы обеспечить совместимость приложения, лучше использовать открытые функции.</span><span class="sxs-lookup"><span data-stu-id="89d3d-120">To maintain the compatibility of your application, it is better to use public functions instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="89d3d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="89d3d-121">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="89d3d-122">**Целевая платформа**</span><span class="sxs-lookup"><span data-stu-id="89d3d-122">**Target Platform**</span></span> | <span data-ttu-id="89d3d-123">Windows</span><span class="sxs-lookup"><span data-stu-id="89d3d-123">Windows</span></span> |
| <span data-ttu-id="89d3d-124">**Header**</span><span class="sxs-lookup"><span data-stu-id="89d3d-124">**Header**</span></span> | <span data-ttu-id="89d3d-125">нтетв. h</span><span class="sxs-lookup"><span data-stu-id="89d3d-125">ntetw.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="89d3d-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89d3d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89d3d-127">EventWrite</span><span class="sxs-lookup"><span data-stu-id="89d3d-127">EventWrite</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[<span data-ttu-id="89d3d-128">евентвритикс</span><span class="sxs-lookup"><span data-stu-id="89d3d-128">EventWriteEx</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
