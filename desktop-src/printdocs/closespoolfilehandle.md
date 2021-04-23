---
description: Функция Клосеспулфилехандле закрывает обработчик файла очереди, связанного с текущим заданием печати, отправленным приложением.
ms.assetid: e2c0e68f-b72e-4a97-ba18-8943bc5789c1
title: Функция Клосеспулфилехандле (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CloseSpoolFileHandle
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: c808bddde5b9b4e4a87a8608c1efb3999ce1f391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673633"
---
# <a name="closespoolfilehandle-function"></a><span data-ttu-id="3dda7-103">Функция Клосеспулфилехандле</span><span class="sxs-lookup"><span data-stu-id="3dda7-103">CloseSpoolFileHandle function</span></span>

<span data-ttu-id="3dda7-104">Функция **клосеспулфилехандле** закрывает обработчик файла очереди, связанного с текущим заданием печати, отправленным приложением.</span><span class="sxs-lookup"><span data-stu-id="3dda7-104">The **CloseSpoolFileHandle** function closes a handle to a spool file associated with the print job currently submitted by the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dda7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3dda7-105">Syntax</span></span>


```C++
BOOL CloseSpoolFileHandle(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile
);
```



## <a name="parameters"></a><span data-ttu-id="3dda7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3dda7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dda7-107">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3dda7-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dda7-108">Маркер принтера, которому было отправлено задание.</span><span class="sxs-lookup"><span data-stu-id="3dda7-108">A handle to the printer to which the job was submitted.</span></span> <span data-ttu-id="3dda7-109">Это должен быть тот же маркер, который использовался для получения *хспулфиле* с [**жетспулфилехандле**](getspoolfilehandle.md).</span><span class="sxs-lookup"><span data-stu-id="3dda7-109">This should be the same handle that was used to obtain *hSpoolFile* with [**GetSpoolFileHandle**](getspoolfilehandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dda7-110">*хспулфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3dda7-110">*hSpoolFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dda7-111">Маркер закрытого файла очереди.</span><span class="sxs-lookup"><span data-stu-id="3dda7-111">A handle to the spool file being closed.</span></span> <span data-ttu-id="3dda7-112">Если [**коммитспулдата**](commitspooldata.md) не вызывался с момента вызова [**жетспулфилехандле**](getspoolfilehandle.md) , это должен быть тот же маркер, который был возвращен **жетспулфилехандле**.</span><span class="sxs-lookup"><span data-stu-id="3dda7-112">If [**CommitSpoolData**](commitspooldata.md) has not been called since [**GetSpoolFileHandle**](getspoolfilehandle.md) was called, then this should be the same handle that was returned by **GetSpoolFileHandle**.</span></span> <span data-ttu-id="3dda7-113">В противном случае он должен быть маркером, возвращенным последним вызовом **коммитспулдата**.</span><span class="sxs-lookup"><span data-stu-id="3dda7-113">Otherwise, it should be the handle that was returned by the most recent call to **CommitSpoolData**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dda7-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3dda7-114">Return value</span></span>

<span data-ttu-id="3dda7-115">**Значение true**, если оно выполняется, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3dda7-115">**TRUE**, if it succeeds, **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dda7-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3dda7-116">Remarks</span></span>

<span data-ttu-id="3dda7-117">Приложение не должно вызывать [**клосепринтер**](closeprinter.md) на *хпринтер* до тех пор, пока он не получал доступ к файлу очереди в последний раз.</span><span class="sxs-lookup"><span data-stu-id="3dda7-117">Your application must not call [**ClosePrinter**](closeprinter.md) on *hPrinter* until after it has accessed the spool file for the last time.</span></span> <span data-ttu-id="3dda7-118">Затем следует вызвать **клосеспулфилехандле** , за которым следует **клосепринтер**.</span><span class="sxs-lookup"><span data-stu-id="3dda7-118">Then it should call **CloseSpoolFileHandle** followed by **ClosePrinter**.</span></span> <span data-ttu-id="3dda7-119">Попытки доступа к буферу файла очереди после закрытия исходного *хпринтер* завершатся ошибкой, даже если сам обработчик файла не был закрыт.</span><span class="sxs-lookup"><span data-stu-id="3dda7-119">Attempts to access the spool file handle after the original *hPrinter* has been closed will fail even if the file handle itself has not been closed.</span></span> <span data-ttu-id="3dda7-120">**Клосеспулфилехандле** завершится ошибкой, если сначала вызывается **клосепринтер** .</span><span class="sxs-lookup"><span data-stu-id="3dda7-120">**CloseSpoolFileHandle** will fail if **ClosePrinter** is called first.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dda7-121">Требования</span><span class="sxs-lookup"><span data-stu-id="3dda7-121">Requirements</span></span>



| <span data-ttu-id="3dda7-122">Требование</span><span class="sxs-lookup"><span data-stu-id="3dda7-122">Requirement</span></span> | <span data-ttu-id="3dda7-123">Значение</span><span class="sxs-lookup"><span data-stu-id="3dda7-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dda7-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3dda7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3dda7-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3dda7-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="3dda7-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3dda7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3dda7-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3dda7-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3dda7-128">Header</span><span class="sxs-lookup"><span data-stu-id="3dda7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dda7-129"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3dda7-129"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3dda7-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3dda7-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="3dda7-131"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3dda7-131"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="3dda7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3dda7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dda7-133"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="3dda7-133"><dt>WinSpool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="3dda7-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3dda7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dda7-135">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="3dda7-135">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3dda7-136">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="3dda7-136">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="3dda7-137">**клосепринтер**</span><span class="sxs-lookup"><span data-stu-id="3dda7-137">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="3dda7-138">**жетспулфилехандле**</span><span class="sxs-lookup"><span data-stu-id="3dda7-138">**GetSpoolFileHandle**</span></span>](getspoolfilehandle.md)
</dt> </dl>

 

 




