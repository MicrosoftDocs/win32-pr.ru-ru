---
description: Метод размещения \_ ErrorLog указывает журнал ошибок для объекта.
ms.assetid: 39da3fb0-57d3-452f-b2ae-6dcd84fa5c8e
title: 'Иамсетеррорлог: метод ut_ErrorLog:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog.put_ErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 189f0fed57d67d7632d07839ee82dd13494eb418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675296"
---
# <a name="iamseterrorlogput_errorlog-method"></a><span data-ttu-id="168a4-103">Иамсетеррорлог: метод:p UT \_ ErrorLog</span><span class="sxs-lookup"><span data-stu-id="168a4-103">IAMSetErrorLog::put\_ErrorLog method</span></span>

> [!Note]  
> <span data-ttu-id="168a4-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="168a4-104">\[Deprecated.</span></span> <span data-ttu-id="168a4-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="168a4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="168a4-106">`put_ErrorLog`Метод задает журнал ошибок для объекта.</span><span class="sxs-lookup"><span data-stu-id="168a4-106">The `put_ErrorLog` method specifies an error log for the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="168a4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="168a4-107">Syntax</span></span>


```C++
HRESULT put_ErrorLog(
  [in] IAMErrorLog *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="168a4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="168a4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="168a4-109">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="168a4-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="168a4-110">Указатель на интерфейс [**иамеррорлог**](iamerrorlog.md) журнала ошибок.</span><span class="sxs-lookup"><span data-stu-id="168a4-110">Pointer to the error log's [**IAMErrorLog**](iamerrorlog.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="168a4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="168a4-111">Return value</span></span>

<span data-ttu-id="168a4-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="168a4-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="168a4-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="168a4-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="168a4-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="168a4-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="168a4-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="168a4-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="168a4-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="168a4-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="168a4-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="168a4-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="168a4-118">Требования</span><span class="sxs-lookup"><span data-stu-id="168a4-118">Requirements</span></span>



| <span data-ttu-id="168a4-119">Требование</span><span class="sxs-lookup"><span data-stu-id="168a4-119">Requirement</span></span> | <span data-ttu-id="168a4-120">Значение</span><span class="sxs-lookup"><span data-stu-id="168a4-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="168a4-121">Header</span><span class="sxs-lookup"><span data-stu-id="168a4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="168a4-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="168a4-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="168a4-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="168a4-123">Library</span></span><br/> | <dl> <span data-ttu-id="168a4-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="168a4-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="168a4-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="168a4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="168a4-126">**Интерфейс Иамсетеррорлог**</span><span class="sxs-lookup"><span data-stu-id="168a4-126">**IAMSetErrorLog Interface**</span></span>](iamseterrorlog.md)
</dt> <dt>

[<span data-ttu-id="168a4-127">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="168a4-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




