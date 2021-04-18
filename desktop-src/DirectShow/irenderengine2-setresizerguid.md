---
description: Метод Сетресизергуид задает идентификатор CLSID пользовательского фильтра изменения размера видео.
ms.assetid: 709a6e7f-64ae-406d-bb6d-29f6c65b63a8
title: 'Метод IRenderEngine2:: Сетресизергуид (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2.SetResizerGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 864053c2c5def6ef1b23ca2c2ee712664e132079
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679842"
---
# <a name="irenderengine2setresizerguid-method"></a><span data-ttu-id="5f624-103">Метод IRenderEngine2:: Сетресизергуид</span><span class="sxs-lookup"><span data-stu-id="5f624-103">IRenderEngine2::SetResizerGUID method</span></span>

> [!Note]  
> <span data-ttu-id="5f624-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="5f624-104">\[Deprecated.</span></span> <span data-ttu-id="5f624-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5f624-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5f624-106">`SetResizerGUID`Метод задает идентификатор CLSID пользовательского фильтра изменения размера видео.</span><span class="sxs-lookup"><span data-stu-id="5f624-106">The `SetResizerGUID` method specifies the CLSID of a custom video resizing filter.</span></span> <span data-ttu-id="5f624-107">Вызовите этот метод, чтобы заменить применяемый по умолчанию фильтр изменения размера, используемый службами редактирования DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5f624-107">Call this method to replace the default resizing filter used by DirectShow Editing Services.</span></span> <span data-ttu-id="5f624-108">Фильтр должен быть зарегистрирован в системе пользователя как COM-объект и должен поддерживать интерфейс [**иресизе**](iresize.md) .</span><span class="sxs-lookup"><span data-stu-id="5f624-108">Your filter must be registered as a COM object on the user's system, and it must support the [**IResize**](iresize.md) interface.</span></span>

<span data-ttu-id="5f624-109">Вызовите этот метод перед вызовом [**ирендеренгине:: коннектфронтенд**](irenderengine-connectfrontend.md).</span><span class="sxs-lookup"><span data-stu-id="5f624-109">Call this method before calling [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5f624-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f624-110">Syntax</span></span>


```C++
HRESULT SetResizerGUID(
  [in] GUID ResizerGuid
);
```



## <a name="parameters"></a><span data-ttu-id="5f624-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f624-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f624-112">*Ресизергуид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5f624-112">*ResizerGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f624-113">Идентификатор CLSID фильтра.</span><span class="sxs-lookup"><span data-stu-id="5f624-113">The CLSID of the filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f624-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f624-114">Return value</span></span>

<span data-ttu-id="5f624-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5f624-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5f624-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5f624-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f624-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5f624-117">Remarks</span></span>

<span data-ttu-id="5f624-118">Чтобы вернуться к измененному по умолчанию размеру DES, используйте следующий идентификатор CLSID:</span><span class="sxs-lookup"><span data-stu-id="5f624-118">To revert to the default DES resizer, use the following CLSID:</span></span>


```C++
// {F97B8A60-31AD-11CF-B2DE-00DD01101B85}
DEFINE_GUID(CLSID_Resize, 
0xF97B8A60, 0x31AD, 0x11CF, 0xB2, 0xDE, 0x00, 0xDD, 0x01, 0x10, 0x1B, 0x85);
```



> [!Note]  
> <span data-ttu-id="5f624-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="5f624-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5f624-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5f624-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5f624-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="5f624-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5f624-122">Требования</span><span class="sxs-lookup"><span data-stu-id="5f624-122">Requirements</span></span>



| <span data-ttu-id="5f624-123">Требование</span><span class="sxs-lookup"><span data-stu-id="5f624-123">Requirement</span></span> | <span data-ttu-id="5f624-124">Значение</span><span class="sxs-lookup"><span data-stu-id="5f624-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f624-125">Версия</span><span class="sxs-lookup"><span data-stu-id="5f624-125">Version</span></span><br/> | <span data-ttu-id="5f624-126">DirectX 9,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="5f624-126">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="5f624-127">Header</span><span class="sxs-lookup"><span data-stu-id="5f624-127">Header</span></span><br/>  | <dl> <span data-ttu-id="5f624-128"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f624-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5f624-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5f624-129">Library</span></span><br/> | <dl> <span data-ttu-id="5f624-130"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f624-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f624-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f624-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f624-132">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="5f624-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="5f624-133">**Интерфейс IRenderEngine2**</span><span class="sxs-lookup"><span data-stu-id="5f624-133">**IRenderEngine2 Interface**</span></span>](irenderengine2.md)
</dt> </dl>

 

 




