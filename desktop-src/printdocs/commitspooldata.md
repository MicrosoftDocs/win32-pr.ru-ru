---
description: Функция Коммитспулдата уведомляет Диспетчер очереди печати о том, что указанный объем данных записан в указанный файл очереди и готов к отображению.
ms.assetid: cb8899e0-2fdf-4928-adff-17ef5af39f63
title: Функция Коммитспулдата (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommitSpoolData
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: fa90cb1344e7c087a601a74991598e509daed226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909379"
---
# <a name="commitspooldata-function"></a><span data-ttu-id="ba330-103">Функция Коммитспулдата</span><span class="sxs-lookup"><span data-stu-id="ba330-103">CommitSpoolData function</span></span>

<span data-ttu-id="ba330-104">Функция **коммитспулдата** уведомляет Диспетчер очереди печати о том, что указанный объем данных записан в указанный файл очереди и готов к отображению.</span><span class="sxs-lookup"><span data-stu-id="ba330-104">The **CommitSpoolData** function notifies the print spooler that a specified amount of data has been written to a specified spool file and is ready to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba330-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba330-105">Syntax</span></span>


```C++
HANDLE CommitSpoolData(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile,
       DWORD  cbCommit
);
```



## <a name="parameters"></a><span data-ttu-id="ba330-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba330-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba330-107">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ba330-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba330-108">Маркер принтера, которому было отправлено задание.</span><span class="sxs-lookup"><span data-stu-id="ba330-108">A handle to the printer to which the job was submitted.</span></span> <span data-ttu-id="ba330-109">Это должен быть тот же маркер, который использовался для получения *хспулфиле* с [**жетспулфилехандле**](getspoolfilehandle.md).</span><span class="sxs-lookup"><span data-stu-id="ba330-109">This should be the same handle that was used to obtain *hSpoolFile* with [**GetSpoolFileHandle**](getspoolfilehandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba330-110">*хспулфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ba330-110">*hSpoolFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba330-111">Изменяемый обработчик файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="ba330-111">A handle to the spool file being changed.</span></span> <span data-ttu-id="ba330-112">При первом вызове **коммитспулдата** это должен быть тот же маркер, который был возвращен [**жетспулфилехандле**](getspoolfilehandle.md).</span><span class="sxs-lookup"><span data-stu-id="ba330-112">On the first call of **CommitSpoolData**, this should be the same handle that was returned by [**GetSpoolFileHandle**](getspoolfilehandle.md).</span></span> <span data-ttu-id="ba330-113">Последующие вызовы **коммитспулдата** должны передавать маркер, возвращенный предыдущим вызовом.</span><span class="sxs-lookup"><span data-stu-id="ba330-113">Subsequent calls to **CommitSpoolData** should pass the handle returned by the preceding call.</span></span> <span data-ttu-id="ba330-114">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="ba330-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ba330-115">*кбкоммит*</span><span class="sxs-lookup"><span data-stu-id="ba330-115">*cbCommit*</span></span> 
</dt> <dd>

<span data-ttu-id="ba330-116">Число байтов, зафиксированных для диспетчера очереди печати.</span><span class="sxs-lookup"><span data-stu-id="ba330-116">The number of bytes committed to the print spooler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba330-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba330-117">Return value</span></span>

<span data-ttu-id="ba330-118">Если функция завершается с ошибкой, она возвращает маркер в файл очереди.</span><span class="sxs-lookup"><span data-stu-id="ba330-118">If the function succeeds, it returns a handle to the spool file.</span></span>

<span data-ttu-id="ba330-119">Если функция завершается ошибкой, она возвращает НЕДОПУСТИМое \_ \_ значение Handle.</span><span class="sxs-lookup"><span data-stu-id="ba330-119">If the function fails, it returns INVALID\_HANDLE\_VALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba330-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba330-120">Remarks</span></span>

<span data-ttu-id="ba330-121">Приложения, которые отправляют задание печати диспетчера очереди сообщений, могут вызывать [**жетспулфилехандле**](getspoolfilehandle.md) , а затем напрямую записывать данные в обработчик файлов очереди путем вызова [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile).</span><span class="sxs-lookup"><span data-stu-id="ba330-121">Applications submitting a spooler print job can call [**GetSpoolFileHandle**](getspoolfilehandle.md) and then directly write data to the spool file handle by calling [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile).</span></span> <span data-ttu-id="ba330-122">Чтобы уведомить Диспетчер очереди печати, что файл содержит данные, готовые к отображению, приложение должно вызвать **коммитспулдата** и указать количество доступных байтов.</span><span class="sxs-lookup"><span data-stu-id="ba330-122">To notify the print spooler that the file contains data which is ready to be rendered, the application must call **CommitSpoolData** and provide the number of available bytes.</span></span>

<span data-ttu-id="ba330-123">Если **коммитспулдата** вызывается несколько раз, каждый вызов должен использовать файл буферизации, возвращенный предыдущим вызовом.</span><span class="sxs-lookup"><span data-stu-id="ba330-123">If **CommitSpoolData** is called multiple times, each call must use the spool file handle returned by the previous call.</span></span> <span data-ttu-id="ba330-124">Если в файл очереди больше не будет записываться никаких данных, [**клосеспулфилехандле**](closespoolfilehandle.md) должен вызываться для файла, возвращенного последним вызовом метода **коммитспулдата**.</span><span class="sxs-lookup"><span data-stu-id="ba330-124">When no more data will be written to the spool file, [**CloseSpoolFileHandle**](closespoolfilehandle.md) should be called for the file handle returned by the last call to **CommitSpoolData**.</span></span>

<span data-ttu-id="ba330-125">Перед вызовом **коммитспулдата** приложения должны установить указатель файла на расположение, в котором оно было до того, как оно записало данные в файл.</span><span class="sxs-lookup"><span data-stu-id="ba330-125">Before calling **CommitSpoolData**, applications must set the file pointer to the position it had before it wrote data to the file.</span></span> <span data-ttu-id="ba330-126">В процессе подготовки к просмотру данных в файле диспетчера очереди печати он переместит указатель файла очереди *кбкоммит* байт из текущего значения указателя файла.</span><span class="sxs-lookup"><span data-stu-id="ba330-126">In the process of rendering the data in the spooler file, the print spooler will move the spool file pointer *cbCommit* bytes from the current value of file pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba330-127">Требования</span><span class="sxs-lookup"><span data-stu-id="ba330-127">Requirements</span></span>



| <span data-ttu-id="ba330-128">Требование</span><span class="sxs-lookup"><span data-stu-id="ba330-128">Requirement</span></span> | <span data-ttu-id="ba330-129">Значение</span><span class="sxs-lookup"><span data-stu-id="ba330-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba330-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba330-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ba330-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ba330-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="ba330-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba330-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ba330-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ba330-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ba330-134">Header</span><span class="sxs-lookup"><span data-stu-id="ba330-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba330-135"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba330-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ba330-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ba330-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="ba330-137"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba330-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ba330-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ba330-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba330-139"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="ba330-139"><dt>WinSpool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="ba330-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba330-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba330-141">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="ba330-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ba330-142">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="ba330-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ba330-143">**жетспулфилехандле**</span><span class="sxs-lookup"><span data-stu-id="ba330-143">**GetSpoolFileHandle**</span></span>](getspoolfilehandle.md)
</dt> <dt>

[<span data-ttu-id="ba330-144">**клосеспулфилехандле**</span><span class="sxs-lookup"><span data-stu-id="ba330-144">**CloseSpoolFileHandle**</span></span>](closespoolfilehandle.md)
</dt> </dl>

 

