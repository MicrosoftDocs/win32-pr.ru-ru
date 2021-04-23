---
description: Функция Експертсубмитевент указывает, что существует условие события и предоставляет структуру данных, описывающую условие.
ms.assetid: 2339b530-427b-4028-aef6-c2cdd1353f77
title: Функция Експертсубмитевент (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertSubmitEvent
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 448d77e9cb009b8aced0aba752526dc08b503066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342762"
---
# <a name="expertsubmitevent-function"></a><span data-ttu-id="a3f4b-103">Функция Експертсубмитевент</span><span class="sxs-lookup"><span data-stu-id="a3f4b-103">ExpertSubmitEvent function</span></span>

<span data-ttu-id="a3f4b-104">Функция **експертсубмитевент** указывает, что существует условие события и предоставляет структуру данных, описывающую условие.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-104">The **ExpertSubmitEvent** function indicates that an event condition exists and provides a data structure that describes the condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3f4b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3f4b-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertSubmitEvent(
  _In_ HEXPERTKEY   hExpertKey,
  _In_ PNMEVENTDATA pExpertEvent
);
```



## <a name="parameters"></a><span data-ttu-id="a3f4b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3f4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3f4b-107">*хексперткэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3f4b-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3f4b-108">Уникальный идентификатор эксперта.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-108">Unique identifier of the expert.</span></span> <span data-ttu-id="a3f4b-109">Сетевой монитор передает *хексперткэй* эксперту при вызове функции [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="a3f4b-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="a3f4b-110">*пекспертевент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3f4b-110">*pExpertEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3f4b-111">Указатель на структуру **нмевентдата** , описывающую условие события.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-111">A pointer to an **NMEVENTDATA** structure that describes the event condition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3f4b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3f4b-112">Return value</span></span>

<span data-ttu-id="a3f4b-113">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-113">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="a3f4b-114">Если функция завершается неудачно, возвращаемое значение указывает причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-114">If the function is unsuccessful, the return value indicates the reason for the failure.</span></span> <span data-ttu-id="a3f4b-115">Если возвращаемое значение — НМЕРР \_ \_ , то эксперт немедленно очищается и возвращает результат.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-115">If the return value is NMERR\_EXPERT\_TERMINATE, the expert immediately cleans up and returns.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3f4b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a3f4b-116">Requirements</span></span>



| <span data-ttu-id="a3f4b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a3f4b-117">Requirement</span></span> | <span data-ttu-id="a3f4b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a3f4b-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a3f4b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3f4b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a3f4b-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a3f4b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a3f4b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3f4b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a3f4b-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a3f4b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a3f4b-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a3f4b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3f4b-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3f4b-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="a3f4b-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a3f4b-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="a3f4b-126"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3f4b-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a3f4b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a3f4b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3f4b-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3f4b-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




