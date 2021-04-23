---
description: Функция Жетспулфилехандле Извлекает маркер для файла очереди, связанного с текущим заданием, отправленным приложением.
ms.assetid: df6f28b3-66a6-4fb7-bdde-40cd7d934c5f
title: Функция Жетспулфилехандле (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSpoolFileHandle
- GetSpoolFileHandleA
- GetSpoolFileHandleW
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9ac4dd4b0db9a59cc0140872ff04f89adaf8b6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081500"
---
# <a name="getspoolfilehandle-function"></a><span data-ttu-id="893c7-103">Функция Жетспулфилехандле</span><span class="sxs-lookup"><span data-stu-id="893c7-103">GetSpoolFileHandle function</span></span>

<span data-ttu-id="893c7-104">Функция **жетспулфилехандле** Извлекает маркер для файла очереди, связанного с текущим заданием, отправленным приложением.</span><span class="sxs-lookup"><span data-stu-id="893c7-104">The **GetSpoolFileHandle** function retrieves a handle for the spool file associated with the job currently submitted by the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="893c7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="893c7-105">Syntax</span></span>


```C++
HANDLE GetSpoolFileHandle(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="893c7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="893c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="893c7-107">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="893c7-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="893c7-108">Маркер принтера, которому было отправлено задание.</span><span class="sxs-lookup"><span data-stu-id="893c7-108">A handle to the printer to which the job was submitted.</span></span> <span data-ttu-id="893c7-109">Это должен быть тот же маркер, который использовался для отправки задания.</span><span class="sxs-lookup"><span data-stu-id="893c7-109">This should be the same handle that was used to submit the job.</span></span> <span data-ttu-id="893c7-110">(Чтобы получить маркер принтера, используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) .)</span><span class="sxs-lookup"><span data-stu-id="893c7-110">(Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="893c7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="893c7-111">Return value</span></span>

<span data-ttu-id="893c7-112">Если функция завершается с ошибкой, она возвращает маркер в файл очереди.</span><span class="sxs-lookup"><span data-stu-id="893c7-112">If the function succeeds, it returns a handle to the spool file.</span></span>

<span data-ttu-id="893c7-113">Если функция завершается ошибкой, она возвращает **недопустимое \_ \_ значение Handle**.</span><span class="sxs-lookup"><span data-stu-id="893c7-113">If the function fails, it returns **INVALID\_HANDLE\_VALUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="893c7-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="893c7-114">Remarks</span></span>

<span data-ttu-id="893c7-115">С помощью обработчика для файла очереди приложение может выполнять запись в файл очереди с вызовами [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) , за которым следует [**коммитспулдата**](commitspooldata.md).</span><span class="sxs-lookup"><span data-stu-id="893c7-115">With the handle to the spool file, your application can write to the spool file with calls to [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) followed by [**CommitSpoolData**](commitspooldata.md).</span></span>

<span data-ttu-id="893c7-116">Приложение не должно вызывать [**клосепринтер**](closeprinter.md) на *хпринтер* до тех пор, пока он не получал доступ к файлу очереди в последний раз.</span><span class="sxs-lookup"><span data-stu-id="893c7-116">Your application must not call [**ClosePrinter**](closeprinter.md) on *hPrinter* until after it has accessed the spool file for the last time.</span></span> <span data-ttu-id="893c7-117">Затем следует вызвать [**клосеспулфилехандле**](closespoolfilehandle.md) , за которым следует **клосепринтер**.</span><span class="sxs-lookup"><span data-stu-id="893c7-117">Then it should call [**CloseSpoolFileHandle**](closespoolfilehandle.md) followed by **ClosePrinter**.</span></span> <span data-ttu-id="893c7-118">Попытки доступа к буферу файла очереди после закрытия исходного *хпринтер* завершатся ошибкой, даже если сам обработчик файла не был закрыт.</span><span class="sxs-lookup"><span data-stu-id="893c7-118">Attempts to access the spool file handle after the original *hPrinter* has been closed will fail even if the file handle itself has not been closed.</span></span> <span data-ttu-id="893c7-119">**Клосеспулфилехандле** будет завершаться ошибкой, если сначала вызывается **клосепринтер** .</span><span class="sxs-lookup"><span data-stu-id="893c7-119">**CloseSpoolFileHandle** will itself fail if **ClosePrinter** is called first.</span></span>

<span data-ttu-id="893c7-120">Эта функция завершится ошибкой, если она вызывается до того, как задание печати завершит работу с очередью.</span><span class="sxs-lookup"><span data-stu-id="893c7-120">This function will fail if it is called before the print job has finished spooling.</span></span>

## <a name="requirements"></a><span data-ttu-id="893c7-121">Требования</span><span class="sxs-lookup"><span data-stu-id="893c7-121">Requirements</span></span>



| <span data-ttu-id="893c7-122">Требование</span><span class="sxs-lookup"><span data-stu-id="893c7-122">Requirement</span></span> | <span data-ttu-id="893c7-123">Значение</span><span class="sxs-lookup"><span data-stu-id="893c7-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="893c7-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="893c7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="893c7-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="893c7-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="893c7-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="893c7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="893c7-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="893c7-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="893c7-128">Header</span><span class="sxs-lookup"><span data-stu-id="893c7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="893c7-129"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="893c7-129"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="893c7-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="893c7-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="893c7-131"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="893c7-131"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="893c7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="893c7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="893c7-133"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="893c7-133"><dt>WinSpool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="893c7-134">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="893c7-134">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="893c7-135">**Жетспулфилехандлев** (Юникод) и **жетспулфилехандлеа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="893c7-135">**GetSpoolFileHandleW** (Unicode) and **GetSpoolFileHandleA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="893c7-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="893c7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="893c7-137">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="893c7-137">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="893c7-138">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="893c7-138">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="893c7-139">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="893c7-139">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="893c7-140">**аддпринтер**</span><span class="sxs-lookup"><span data-stu-id="893c7-140">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="893c7-141">**клосепринтер**</span><span class="sxs-lookup"><span data-stu-id="893c7-141">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="893c7-142">**клосеспулфилехандле**</span><span class="sxs-lookup"><span data-stu-id="893c7-142">**CloseSpoolFileHandle**</span></span>](closespoolfilehandle.md)
</dt> <dt>

[<span data-ttu-id="893c7-143">**коммитспулдата**</span><span class="sxs-lookup"><span data-stu-id="893c7-143">**CommitSpoolData**</span></span>](commitspooldata.md)
</dt> </dl>

 

