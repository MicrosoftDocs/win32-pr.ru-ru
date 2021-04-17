---
description: Метод Жетнекстсрцекс извлекает следующий источник после указанного источника.
ms.assetid: cda3d079-eeb5-42a9-8854-5c90ae0e2c07
title: 'Метод Иамтимелинетракк:: Жетнекстсрцекс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrcEx
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 274a4f6800d995e2b456dbd55adf81cf82aa84a9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685240"
---
# <a name="iamtimelinetrackgetnextsrcex-method"></a><span data-ttu-id="2787a-103">Метод Иамтимелинетракк:: Жетнекстсрцекс</span><span class="sxs-lookup"><span data-stu-id="2787a-103">IAMTimelineTrack::GetNextSrcEx method</span></span>

> [!Note]  
> <span data-ttu-id="2787a-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="2787a-104">\[Deprecated.</span></span> <span data-ttu-id="2787a-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2787a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2787a-106">`GetNextSrcEx`Метод извлекает следующий источник после указанного источника.</span><span class="sxs-lookup"><span data-stu-id="2787a-106">The `GetNextSrcEx` method retrieves the next source after the specified source.</span></span>

## <a name="syntax"></a><span data-ttu-id="2787a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2787a-107">Syntax</span></span>


```C++
HRESULT GetNextSrcEx(
        IAMTimelineObj *pLast,
  [out] IAMTimelineObj **ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="2787a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2787a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2787a-109">*пласт*</span><span class="sxs-lookup"><span data-stu-id="2787a-109">*pLast*</span></span> 
</dt> <dd>

<span data-ttu-id="2787a-110">Указатель на предыдущий исходный объект или **значение NULL** для получения первого источника в дорожке.</span><span class="sxs-lookup"><span data-stu-id="2787a-110">Pointer to the previous source object, or **NULL** to retrieve the first source in the track.</span></span>

</dd> <dt>

<span data-ttu-id="2787a-111">*ппнекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2787a-111">*ppNext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2787a-112">Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) следующего исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="2787a-112">Receives a pointer to the next source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2787a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2787a-113">Return value</span></span>

<span data-ttu-id="2787a-114">Возвращает \_ значение ОК, если метод получает источник, или \_ false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2787a-114">Returns S\_OK if the method retrieves a source, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2787a-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2787a-115">Remarks</span></span>

<span data-ttu-id="2787a-116">Если метод возвращает значение " \_ ОК", возвращаемый им интерфейс **иамтимелинеобж** имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="2787a-116">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="2787a-117">Не забудьте освободить интерфейс по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="2787a-117">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="2787a-118">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="2787a-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2787a-119">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2787a-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2787a-120">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2787a-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2787a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2787a-121">Requirements</span></span>



| <span data-ttu-id="2787a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2787a-122">Requirement</span></span> | <span data-ttu-id="2787a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2787a-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2787a-124">Header</span><span class="sxs-lookup"><span data-stu-id="2787a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2787a-125"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="2787a-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2787a-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2787a-126">Library</span></span><br/> | <dl> <span data-ttu-id="2787a-127"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2787a-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2787a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2787a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2787a-129">**Интерфейс Иамтимелинетракк**</span><span class="sxs-lookup"><span data-stu-id="2787a-129">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="2787a-130">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="2787a-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




