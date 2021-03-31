---
title: Иорпкдебугнотифи Серверфиллбуффер, метод
description: Отправляет данные из отладчика сервера в клиентский отладчик.
ms.assetid: 58813f28-6e32-478c-8b12-8cf0ebe01973
keywords:
- COM-метод Серверфиллбуффер
- Метод Серверфиллбуффер COM, интерфейс Иорпкдебугнотифи
- Интерфейс Иорпкдебугнотифи COM, метод Серверфиллбуффер
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ServerFillBuffer
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffac861e3ac2d35d6d738755e2e5d7814ec41b4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803928"
---
# <a name="iorpcdebugnotifyserverfillbuffer-method"></a><span data-ttu-id="17d11-106">Метод Иорпкдебугнотифи:: Серверфиллбуффер</span><span class="sxs-lookup"><span data-stu-id="17d11-106">IOrpcDebugNotify::ServerFillBuffer method</span></span>

<span data-ttu-id="17d11-107">Отправляет данные из отладчика сервера в клиентский отладчик.</span><span class="sxs-lookup"><span data-stu-id="17d11-107">Sends data from the server debugger to the client debugger.</span></span>

> [!Note]  
> <span data-ttu-id="17d11-108">Библиотека импорта, содержащая функцию **серверфиллбуффер** , не включена в пакет средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="17d11-108">An import library containing the **ServerFillBuffer** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="17d11-109">Приложение может использовать функции [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) и [**Ошибка GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) для получения указателя на функцию [**дллдебугобжектрпчук**](dlldebugobjectrpchook.md) из oleaut.dll и предоставления этой функции через интерфейс [**иорпкдебугнотифи**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="17d11-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="17d11-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17d11-110">Syntax</span></span>


```C++
void ServerFillBuffer(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="17d11-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="17d11-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17d11-112">*лпорпкдебугалл*</span><span class="sxs-lookup"><span data-stu-id="17d11-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="17d11-113">Указатель на структуру [**ОРПК \_ dbg \_ ALL**](orpc-dbg-all.md) , содержащую сведения об уведомлении, которые система com RPC передает отладчику.</span><span class="sxs-lookup"><span data-stu-id="17d11-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17d11-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17d11-114">Return value</span></span>

<span data-ttu-id="17d11-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="17d11-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="17d11-116">Требования</span><span class="sxs-lookup"><span data-stu-id="17d11-116">Requirements</span></span>



| <span data-ttu-id="17d11-117">Требование</span><span class="sxs-lookup"><span data-stu-id="17d11-117">Requirement</span></span> | <span data-ttu-id="17d11-118">Значение</span><span class="sxs-lookup"><span data-stu-id="17d11-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="17d11-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="17d11-119">Minimum supported client</span></span><br/> | <span data-ttu-id="17d11-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="17d11-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="17d11-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="17d11-121">Minimum supported server</span></span><br/> | <span data-ttu-id="17d11-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="17d11-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="17d11-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="17d11-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="17d11-124"><dt>Н/Д</dt></span><span class="sxs-lookup"><span data-stu-id="17d11-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="17d11-125">IDL</span><span class="sxs-lookup"><span data-stu-id="17d11-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17d11-126"><dt>Н/Д</dt></span><span class="sxs-lookup"><span data-stu-id="17d11-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17d11-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17d11-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17d11-128">**\_аргументы инициализации \_ ОРПК**</span><span class="sxs-lookup"><span data-stu-id="17d11-128">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="17d11-129">**дллдебугобжектрпчук**</span><span class="sxs-lookup"><span data-stu-id="17d11-129">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="17d11-130">**иорпкдебугнотифи**</span><span class="sxs-lookup"><span data-stu-id="17d11-130">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

