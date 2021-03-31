---
description: Функция Експертжетстартупинфо извлекает сведения о конфигурации запуска эксперта.
ms.assetid: 15f080ed-50b7-40c6-b283-dbe416a2b0e9
title: Функция Експертжетстартупинфо (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetStartupInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f34ecc3d0c3eeb085d2a7c0f8c4cb0426663093c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423682"
---
# <a name="expertgetstartupinfo-function"></a><span data-ttu-id="8d368-103">Функция Експертжетстартупинфо</span><span class="sxs-lookup"><span data-stu-id="8d368-103">ExpertGetStartupInfo function</span></span>

<span data-ttu-id="8d368-104">Функция **експертжетстартупинфо** извлекает сведения о конфигурации запуска эксперта.</span><span class="sxs-lookup"><span data-stu-id="8d368-104">The **ExpertGetStartupInfo** function retrieves the startup configuration information for the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d368-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d368-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertGetStartupInfo(
  _In_  HEXPERTKEY         hExpertKey,
  _Out_ PEXPERTSTARTUPINFO pExpertStartupInfo
);
```



## <a name="parameters"></a><span data-ttu-id="8d368-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d368-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d368-107">*хексперткэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d368-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d368-108">Уникальный идентификатор эксперта.</span><span class="sxs-lookup"><span data-stu-id="8d368-108">Unique expert identifier.</span></span> <span data-ttu-id="8d368-109">Сетевой монитор передает *хексперткэй* эксперту при вызове функции [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="8d368-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="8d368-110">*пекспертстартупинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8d368-110">*pExpertStartupInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d368-111">Указатель на структуру [експертстартупинфо](expertstartupinfo.md) , содержащую сведения о запуске.</span><span class="sxs-lookup"><span data-stu-id="8d368-111">Pointer to an [EXPERTSTARTUPINFO](expertstartupinfo.md) structure that contains startup information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d368-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d368-112">Return value</span></span>

<span data-ttu-id="8d368-113">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="8d368-113">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="8d368-114">Если функция завершается неудачно, возвращается значение НМЕРР.</span><span class="sxs-lookup"><span data-stu-id="8d368-114">If the function is unsuccessful, the return value is NMERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d368-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d368-115">Remarks</span></span>

<span data-ttu-id="8d368-116">Функция **експертжетстартупинфо** используется, если эксперт должен определить используемые сведения о запуске.</span><span class="sxs-lookup"><span data-stu-id="8d368-116">The **ExpertGetStartupInfo** function is used if the expert must determine the startup information that is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d368-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8d368-117">Requirements</span></span>



| <span data-ttu-id="8d368-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8d368-118">Requirement</span></span> | <span data-ttu-id="8d368-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8d368-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8d368-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d368-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8d368-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8d368-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8d368-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d368-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8d368-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8d368-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8d368-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8d368-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d368-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d368-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="8d368-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8d368-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="8d368-127"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d368-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="8d368-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8d368-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d368-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d368-129"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




