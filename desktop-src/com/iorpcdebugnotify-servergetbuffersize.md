---
title: Иорпкдебугнотифи Сервержетбуфферсизе, метод
description: Извлекает размер буфера RPC из отладчика на стороне сервера.
ms.assetid: 1e9ef194-c85b-4f6d-8b89-1f7ee6941189
keywords:
- COM-метод Сервержетбуфферсизе
- Метод Сервержетбуфферсизе COM, интерфейс Иорпкдебугнотифи
- Интерфейс Иорпкдебугнотифи COM, метод Сервержетбуфферсизе
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ServerGetBufferSize
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d461670cc65f5cfcb433a52529e724a1c54bede
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989386"
---
# <a name="iorpcdebugnotifyservergetbuffersize-method"></a><span data-ttu-id="44904-106">Метод Иорпкдебугнотифи:: Сервержетбуфферсизе</span><span class="sxs-lookup"><span data-stu-id="44904-106">IOrpcDebugNotify::ServerGetBufferSize method</span></span>

<span data-ttu-id="44904-107">Извлекает размер буфера RPC из отладчика на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="44904-107">Retrieves the RPC buffer size from the server-side debugger.</span></span>

> [!Note]  
> <span data-ttu-id="44904-108">Библиотека импорта, содержащая функцию **сервержетбуфферсизе** , не включена в пакет средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="44904-108">An import library containing the **ServerGetBufferSize** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="44904-109">Приложение может использовать функции [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) и [**Ошибка GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) для получения указателя на функцию [**дллдебугобжектрпчук**](dlldebugobjectrpchook.md) из oleaut.dll и предоставления этой функции через интерфейс [**иорпкдебугнотифи**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="44904-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="44904-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44904-110">Syntax</span></span>


```C++
void ServerGetBufferSize(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="44904-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="44904-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44904-112">*лпорпкдебугалл*</span><span class="sxs-lookup"><span data-stu-id="44904-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="44904-113">Указатель на структуру [**ОРПК \_ dbg \_ ALL**](orpc-dbg-all.md) , содержащую сведения об уведомлении, которые система com RPC передает отладчику.</span><span class="sxs-lookup"><span data-stu-id="44904-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44904-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44904-114">Return value</span></span>

<span data-ttu-id="44904-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="44904-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="44904-116">Требования</span><span class="sxs-lookup"><span data-stu-id="44904-116">Requirements</span></span>



| <span data-ttu-id="44904-117">Требование</span><span class="sxs-lookup"><span data-stu-id="44904-117">Requirement</span></span> | <span data-ttu-id="44904-118">Значение</span><span class="sxs-lookup"><span data-stu-id="44904-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="44904-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44904-119">Minimum supported client</span></span><br/> | <span data-ttu-id="44904-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="44904-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="44904-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44904-121">Minimum supported server</span></span><br/> | <span data-ttu-id="44904-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="44904-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="44904-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="44904-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="44904-124"><dt>Н/Д</dt></span><span class="sxs-lookup"><span data-stu-id="44904-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="44904-125">IDL</span><span class="sxs-lookup"><span data-stu-id="44904-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="44904-126"><dt>Н/Д</dt></span><span class="sxs-lookup"><span data-stu-id="44904-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44904-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44904-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44904-128">**\_аргументы инициализации \_ ОРПК**</span><span class="sxs-lookup"><span data-stu-id="44904-128">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="44904-129">**дллдебугобжектрпчук**</span><span class="sxs-lookup"><span data-stu-id="44904-129">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="44904-130">**иорпкдебугнотифи**</span><span class="sxs-lookup"><span data-stu-id="44904-130">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

