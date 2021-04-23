---
title: Функция Мсимтфисвиндовфилтеред
description: Функция Мсимтфисвиндовфилтеред проверяет, фильтруется ли заданное окно по АИММ (активным диспетчером метода ввода).
ms.assetid: 1f5e98f1-3626-4aa5-b2da-b6bc48d02184
keywords:
- Платформа текстовых служб Мсимтфисвиндовфилтеред Function
topic_type:
- apiref
api_name:
- MsimtfIsWindowFiltered
api_location:
- msimtf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70ad9bd9fb61c546ec3e2f1d96d5fc9cf932613a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137043"
---
# <a name="msimtfiswindowfiltered-function"></a><span data-ttu-id="cf224-104">Функция Мсимтфисвиндовфилтеред</span><span class="sxs-lookup"><span data-stu-id="cf224-104">MsimtfIsWindowFiltered function</span></span>

<span data-ttu-id="cf224-105">Функция **мсимтфисвиндовфилтеред** проверяет, фильтруется ли заданное окно по АИММ (активным диспетчером метода ввода).</span><span class="sxs-lookup"><span data-stu-id="cf224-105">The **MsimtfIsWindowFiltered** function tests if the given window is filtered by AIMM (Active Input Method Manager).</span></span>

## <a name="syntax"></a><span data-ttu-id="cf224-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf224-106">Syntax</span></span>


```C++
BOOL CALLBACK MsimtfIsWindowFiltered(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="cf224-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf224-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf224-108">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf224-108">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf224-109">Проверяемый описатель окна.</span><span class="sxs-lookup"><span data-stu-id="cf224-109">A window handle to be tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf224-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf224-110">Return value</span></span>



| <span data-ttu-id="cf224-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cf224-111">Return code</span></span>                                                                          | <span data-ttu-id="cf224-112">Описание</span><span class="sxs-lookup"><span data-stu-id="cf224-112">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cf224-113"><dt>**УСЛОВИЯ**</dt></span><span class="sxs-lookup"><span data-stu-id="cf224-113"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="cf224-114">Если это окно фильтруется по активному диспетчеру методов ввода.</span><span class="sxs-lookup"><span data-stu-id="cf224-114">If this window is filtered by Active Input Method Manager.</span></span><br/>     |
| <dl> <span data-ttu-id="cf224-115"><dt>**ISFALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="cf224-115"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="cf224-116">Если это окно не фильтруется с помощью активного диспетчера методов ввода.</span><span class="sxs-lookup"><span data-stu-id="cf224-116">If this window is not filtered by Active Input Method Manager.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cf224-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf224-117">Remarks</span></span>

<span data-ttu-id="cf224-118">Окно может быть отфильтровано по Иактивеиммапп:: Филтерклиентвиндовс.</span><span class="sxs-lookup"><span data-stu-id="cf224-118">A window can be filtered by IActiveIMMApp::FilterClientWindows.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf224-119">Требования</span><span class="sxs-lookup"><span data-stu-id="cf224-119">Requirements</span></span>



| <span data-ttu-id="cf224-120">Требование</span><span class="sxs-lookup"><span data-stu-id="cf224-120">Requirement</span></span> | <span data-ttu-id="cf224-121">Значение</span><span class="sxs-lookup"><span data-stu-id="cf224-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf224-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf224-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cf224-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf224-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cf224-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf224-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cf224-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cf224-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf224-126">DLL</span><span class="sxs-lookup"><span data-stu-id="cf224-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf224-127"><dt>Msimtf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf224-127"><dt>Msimtf.dll</dt></span></span> </dl> |



 

 





