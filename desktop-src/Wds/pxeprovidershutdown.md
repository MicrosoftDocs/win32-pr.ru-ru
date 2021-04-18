---
title: Функция обратного вызова Пксепровидершутдовн
description: Вызывается для завершения работы поставщика.
ms.assetid: 436d7428-18f9-4b73-b346-79c9a0738c31
keywords:
- Функция обратного вызова Пксепровидершутдовн службы развертывания Windows
topic_type:
- apiref
api_name:
- PxeProviderShutdown
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17698c5fa1f6ce6bd5443d0244ebc6ce6082ec33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701045"
---
# <a name="pxeprovidershutdown-callback-function"></a><span data-ttu-id="41b50-104">Функция обратного вызова Пксепровидершутдовн</span><span class="sxs-lookup"><span data-stu-id="41b50-104">PxeProviderShutdown callback function</span></span>

<span data-ttu-id="41b50-105">Вызывается для завершения работы поставщика.</span><span class="sxs-lookup"><span data-stu-id="41b50-105">Called to shutdown the provider.</span></span> <span data-ttu-id="41b50-106">Эта функция регистрируется путем вызова функции [**пксерегистеркаллбакк**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) с параметром *каллбакктипе* , для которого задано **\_ \_ Отключение обратного вызова PXE**.</span><span class="sxs-lookup"><span data-stu-id="41b50-106">This function is registered by calling the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function with the *CallbackType* parameter set to **PXE\_CALLBACK\_SHUTDOWN**.</span></span> <span data-ttu-id="41b50-107">После вызова этой функции обработчик *хпровидер* , переданный функции [*пксепровидеринитиализе*](pxeproviderinitialize.md) , больше не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="41b50-107">After this function is called, the *hProvider* handle passed to the [*PxeProviderInitialize*](pxeproviderinitialize.md) function is no longer valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="41b50-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41b50-108">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderShutdown(
  _In_ PVOID pContext
);
```



## <a name="parameters"></a><span data-ttu-id="41b50-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="41b50-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41b50-110">*пконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41b50-110">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41b50-111">Значение контекста, передаваемое функции [**пксерегистеркаллбакк**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="41b50-111">Context value passed to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41b50-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41b50-112">Return value</span></span>

<span data-ttu-id="41b50-113">Если завершение работы поставщика завершается успешно, обратный вызов должен возвращать **ошибку \_ успешно**.</span><span class="sxs-lookup"><span data-stu-id="41b50-113">If the provider shutdown succeeds, the callback should return **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="41b50-114">В случае сбоя должен возвращаться соответствующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="41b50-114">In case of failure, an appropriate error code should be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="41b50-115">Требования</span><span class="sxs-lookup"><span data-stu-id="41b50-115">Requirements</span></span>



| <span data-ttu-id="41b50-116">Требование</span><span class="sxs-lookup"><span data-stu-id="41b50-116">Requirement</span></span> | <span data-ttu-id="41b50-117">Значение</span><span class="sxs-lookup"><span data-stu-id="41b50-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="41b50-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41b50-118">Minimum supported client</span></span><br/> | <span data-ttu-id="41b50-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="41b50-119">None supported</span></span><br/>                                                          |
| <span data-ttu-id="41b50-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41b50-120">Minimum supported server</span></span><br/> | <span data-ttu-id="41b50-121">Windows Server 2008, Windows Server 2003 с пакетом обновления 2 (SP2), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="41b50-121">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41b50-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41b50-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41b50-123">Функции сервера служб развертывания Windows</span><span class="sxs-lookup"><span data-stu-id="41b50-123">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="41b50-124">*пксепровидеринитиализе*</span><span class="sxs-lookup"><span data-stu-id="41b50-124">*PxeProviderInitialize*</span></span>](pxeproviderinitialize.md)
</dt> <dt>

[<span data-ttu-id="41b50-125">**пксерегистеркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="41b50-125">**PxeRegisterCallback**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

 





