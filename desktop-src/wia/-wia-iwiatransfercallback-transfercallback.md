---
description: Предоставляет ход выполнения и другие уведомления во время перемещения.
ms.assetid: 0faba0f8-b318-4c47-85e0-5ce128fe1c82
title: 'Метод Ивиатрансферкаллбакк:: Трансферкаллбакк (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.TransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: f1e2f939a7a3d768fc744c0603563b0a088e08f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692423"
---
# <a name="iwiatransfercallbacktransfercallback-method"></a><span data-ttu-id="a97d2-103">Метод Ивиатрансферкаллбакк:: Трансферкаллбакк</span><span class="sxs-lookup"><span data-stu-id="a97d2-103">IWiaTransferCallback::TransferCallback method</span></span>

<span data-ttu-id="a97d2-104">Предоставляет ход выполнения и другие уведомления во время перемещения.</span><span class="sxs-lookup"><span data-stu-id="a97d2-104">Provides progress and other notifications during a transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a97d2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a97d2-105">Syntax</span></span>


```C++
HRESULT TransferCallback(
  [in] LONG              lFlags,
  [in] WiaTransferParams *pWiaTransferParams
);
```



## <a name="parameters"></a><span data-ttu-id="a97d2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a97d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a97d2-107">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a97d2-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a97d2-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="a97d2-108">Type: **LONG**</span></span>

<span data-ttu-id="a97d2-109">В настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="a97d2-109">Currently unused.</span></span> <span data-ttu-id="a97d2-110">Значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="a97d2-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a97d2-111">*пвиатрансферпарамс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a97d2-111">*pWiaTransferParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a97d2-112">Тип: \**[**виатрансферпарамс**](-wia-wiatransferparams.md) \** _</span><span class="sxs-lookup"><span data-stu-id="a97d2-112">Type: \**[**WiaTransferParams**](-wia-wiatransferparams.md)\** _</span></span>

<span data-ttu-id="a97d2-113">Указывает указатель на структуру [_ *виатрансферпарамс* \*](-wia-wiatransferparams.md) .</span><span class="sxs-lookup"><span data-stu-id="a97d2-113">Specifies a pointer to a [_ *WiaTransferParams*\*](-wia-wiatransferparams.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a97d2-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a97d2-114">Return value</span></span>

<span data-ttu-id="a97d2-115">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a97d2-115">Type: **HRESULT**</span></span>

<span data-ttu-id="a97d2-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a97d2-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a97d2-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a97d2-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a97d2-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a97d2-118">Remarks</span></span>

<span data-ttu-id="a97d2-119">Когда этот метод реализуется с помощью фильтра обработки изображений, при получении образа Windows (WIA) 2,0 минидривер вызывает его во время получения изображения для отправки сообщений о ходе выполнения обратно в приложение.</span><span class="sxs-lookup"><span data-stu-id="a97d2-119">When this method is implemented by an image processing filter, the Windows Image Acquisition (WIA) 2.0 minidriver calls it during image acquisition to send progress messages back to the application.</span></span>

<span data-ttu-id="a97d2-120">Фильтр **ивиатрансферкаллбакк:: трансферкаллбакк** должен делегировать методу **Ивиатрансферкаллбакк:: трансферкаллбакк** обратного вызова приложения.</span><span class="sxs-lookup"><span data-stu-id="a97d2-120">A filter's **IWiaTransferCallback::TransferCallback** must delegate to the application callback's **IWiaTransferCallback::TransferCallback** method.</span></span> <span data-ttu-id="a97d2-121">Обычно поток фильтра фильтрует данные, передаваемые в него, и записывает отфильтрованные данные непосредственно в предоставленный приложением поток.</span><span class="sxs-lookup"><span data-stu-id="a97d2-121">Usually, the filter stream filters the data passed to it and writes the filtered data directly to the application provided stream.</span></span> <span data-ttu-id="a97d2-122">Когда фильтр обработки изображений сохраняет данные между вызовами метода [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) , он также должен изменить значения *лперценткомплете* и *улбитесвриттентокуррентстреам* в структуре [**виатрансферпарамс**](-wia-wiatransferparams.md) .</span><span class="sxs-lookup"><span data-stu-id="a97d2-122">When image processing filter stores data between calls to its [IStream::Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) method, it must also modify the *lPercentComplete* and *ulBytesWrittenToCurrentStream* values in the [**WiaTransferParams**](-wia-wiatransferparams.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a97d2-123">Требования</span><span class="sxs-lookup"><span data-stu-id="a97d2-123">Requirements</span></span>



| <span data-ttu-id="a97d2-124">Требование</span><span class="sxs-lookup"><span data-stu-id="a97d2-124">Requirement</span></span> | <span data-ttu-id="a97d2-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a97d2-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a97d2-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a97d2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a97d2-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a97d2-127">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a97d2-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a97d2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a97d2-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a97d2-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a97d2-130">Header</span><span class="sxs-lookup"><span data-stu-id="a97d2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a97d2-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="a97d2-131"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="a97d2-132">IDL</span><span class="sxs-lookup"><span data-stu-id="a97d2-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a97d2-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a97d2-133"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="a97d2-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a97d2-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="a97d2-135"><dt>Виагуид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a97d2-135"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
