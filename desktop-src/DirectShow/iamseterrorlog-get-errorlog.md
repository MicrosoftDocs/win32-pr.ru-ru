---
description: Метод Get \_ ErrorLog извлекает текущий журнал ошибок для данного объекта.
ms.assetid: 580b8a06-6bf2-49ef-a5fb-5e6df2f09793
title: 'Метод Иамсетеррорлог:: get_ErrorLog (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog.get_ErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 508a73d6475698dca628de7e3bb96001fe13bcd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651795"
---
# <a name="iamseterrorlogget_errorlog-method"></a><span data-ttu-id="9f227-103">Метод Иамсетеррорлог:: Get \_ ErrorLog</span><span class="sxs-lookup"><span data-stu-id="9f227-103">IAMSetErrorLog::get\_ErrorLog method</span></span>

> [!Note]  
> <span data-ttu-id="9f227-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="9f227-104">\[Deprecated.</span></span> <span data-ttu-id="9f227-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9f227-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9f227-106">`get_ErrorLog`Метод извлекает текущий журнал ошибок для данного объекта.</span><span class="sxs-lookup"><span data-stu-id="9f227-106">The `get_ErrorLog` method retrieves the current error log for this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f227-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f227-107">Syntax</span></span>


```C++
HRESULT get_ErrorLog(
  [out, retval] IAMErrorLog **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="9f227-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f227-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f227-109">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="9f227-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9f227-110">Получает указатель на интерфейс [**иамеррорлог**](iamerrorlog.md) журнала ошибок.</span><span class="sxs-lookup"><span data-stu-id="9f227-110">Receives a pointer to the error log's [**IAMErrorLog**](iamerrorlog.md) interface.</span></span> <span data-ttu-id="9f227-111">Если на временной шкале нет журнала ошибок, значение устанавливается равным **null**.</span><span class="sxs-lookup"><span data-stu-id="9f227-111">If the timeline does not have an error log, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f227-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f227-112">Return value</span></span>

<span data-ttu-id="9f227-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="9f227-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9f227-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9f227-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f227-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f227-115">Remarks</span></span>

<span data-ttu-id="9f227-116">Если значение, возвращаемое в *Pval* , не равно **null**, то интерфейс [**иамеррорлог**](iamerrorlog.md) имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="9f227-116">If the value returned in *pVal* is not **NULL**, the [**IAMErrorLog**](iamerrorlog.md) interface has an outstanding reference count.</span></span> <span data-ttu-id="9f227-117">Не забудьте освободить интерфейс по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="9f227-117">Be sure to release the interface when you are done using it.</span></span>

> [!Note]  
> <span data-ttu-id="9f227-118">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="9f227-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9f227-119">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9f227-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9f227-120">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="9f227-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9f227-121">Требования</span><span class="sxs-lookup"><span data-stu-id="9f227-121">Requirements</span></span>



| <span data-ttu-id="9f227-122">Требование</span><span class="sxs-lookup"><span data-stu-id="9f227-122">Requirement</span></span> | <span data-ttu-id="9f227-123">Значение</span><span class="sxs-lookup"><span data-stu-id="9f227-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f227-124">Header</span><span class="sxs-lookup"><span data-stu-id="9f227-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9f227-125"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f227-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9f227-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9f227-126">Library</span></span><br/> | <dl> <span data-ttu-id="9f227-127"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f227-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f227-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f227-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f227-129">**Интерфейс Иамсетеррорлог**</span><span class="sxs-lookup"><span data-stu-id="9f227-129">**IAMSetErrorLog Interface**</span></span>](iamseterrorlog.md)
</dt> <dt>

[<span data-ttu-id="9f227-130">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="9f227-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




