---
title: Функция Дллдебугобжектрпчук
description: Экспортировано библиотеками DLL COM для включения удаленной отладки.
ms.assetid: a0f8bf12-0889-452d-84d0-255c5c143bc1
keywords:
- COM-функция Дллдебугобжектрпчук
topic_type:
- apiref
api_name:
- DllDebugObjectRPCHook
api_location:
- ole32.dll
- API-MS-Win-Core-Com-private-l1-1-0.dll
- ComBase.dll
- API-MS-Win-Core-COM-Private-l1-1-1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62fffe6cc2d9ca650442d0a1c3fea2048fc6c84b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710547"
---
# <a name="dlldebugobjectrpchook-function"></a><span data-ttu-id="d6bf5-104">Функция Дллдебугобжектрпчук</span><span class="sxs-lookup"><span data-stu-id="d6bf5-104">DllDebugObjectRPCHook function</span></span>

<span data-ttu-id="d6bf5-105">Экспортировано библиотеками DLL COM для включения удаленной отладки.</span><span class="sxs-lookup"><span data-stu-id="d6bf5-105">Exported by COM DLLs to enable remote debugging.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6bf5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6bf5-106">Syntax</span></span>


```C++
BOOL WINAPI DllDebugObjectRPCHook(
   BOOL             fTrace,
   LPORPC_INIT_ARGS lpOrpcInitArgs
);
```



## <a name="parameters"></a><span data-ttu-id="d6bf5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6bf5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6bf5-108">*фтраце*</span><span class="sxs-lookup"><span data-stu-id="d6bf5-108">*fTrace*</span></span> 
</dt> <dd>

<span data-ttu-id="d6bf5-109">Если **значение — true**, удаленная отладка включена.</span><span class="sxs-lookup"><span data-stu-id="d6bf5-109">If **TRUE**, remote debugging is enabled.</span></span> <span data-ttu-id="d6bf5-110">Если задано **значение false**, удаленная отладка не включена.</span><span class="sxs-lookup"><span data-stu-id="d6bf5-110">If **FALSE**, remote debugging is not enabled.</span></span>

</dd> <dt>

<span data-ttu-id="d6bf5-111">*лпорпЦинитаргс*</span><span class="sxs-lookup"><span data-stu-id="d6bf5-111">*lpOrpcInitArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="d6bf5-112">Указатель на структуру [**\_ \_ args ОРПК**](orpc-init-args.md) .</span><span class="sxs-lookup"><span data-stu-id="d6bf5-112">A pointer to an [**ORPC\_INIT\_ARGS**](orpc-init-args.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6bf5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6bf5-113">Return value</span></span>

<span data-ttu-id="d6bf5-114">**Значение true** , если выполнено успешно; в противном случае — **false**</span><span class="sxs-lookup"><span data-stu-id="d6bf5-114">**TRUE** if successful, **FALSE** otherwise</span></span>

## <a name="requirements"></a><span data-ttu-id="d6bf5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d6bf5-115">Requirements</span></span>



| <span data-ttu-id="d6bf5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d6bf5-116">Requirement</span></span> | <span data-ttu-id="d6bf5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d6bf5-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d6bf5-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d6bf5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d6bf5-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d6bf5-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d6bf5-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d6bf5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d6bf5-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d6bf5-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d6bf5-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d6bf5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6bf5-123"><dt>Н/Д</dt></span><span class="sxs-lookup"><span data-stu-id="d6bf5-123"><dt>N/A</dt></span></span> </dl>       |
| <span data-ttu-id="d6bf5-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d6bf5-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="d6bf5-125"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6bf5-125"><dt>Ole32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d6bf5-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d6bf5-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6bf5-127"><dt>Ole32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6bf5-127"><dt>Ole32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6bf5-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6bf5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6bf5-129">**ОРПК \_ dbg \_ ALL**</span><span class="sxs-lookup"><span data-stu-id="d6bf5-129">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="d6bf5-130">**\_БУФЕР ОРПК dbg \_**</span><span class="sxs-lookup"><span data-stu-id="d6bf5-130">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="d6bf5-131">**\_аргументы инициализации \_ ОРПК**</span><span class="sxs-lookup"><span data-stu-id="d6bf5-131">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="d6bf5-132">**иорпкдебугнотифи**</span><span class="sxs-lookup"><span data-stu-id="d6bf5-132">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

 





