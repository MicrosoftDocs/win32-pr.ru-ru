---
title: Установка пользовательских процедур ввода-вывода
description: Установка пользовательских процедур ввода-вывода
ms.assetid: 7b26a062-fa52-4de3-b8c8-b9f9167068fc
keywords:
- пользовательские операции ввода-вывода файлов мультимедиа, процедуры
- Ввод-вывод файлов, пользовательские процедуры
- входные и выходные данные (ввод-вывод), пользовательские процедуры
- Ввод-вывод (входные и выходные данные), пользовательские процедуры
- Установка пользовательских процедур ввода-вывода
- пользовательский ввод-вывод
- Функция Ммиоинсталлиопрок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1574b7076e7344fa8e800ef1f18ad13fcfd3f3af
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412952"
---
# <a name="installing-custom-io-procedures"></a><span data-ttu-id="83e65-110">Установка пользовательских процедур ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="83e65-110">Installing Custom I/O Procedures</span></span>

<span data-ttu-id="83e65-111">Для установки процедуры ввода-вывода, связанной с. Расширение имени файла ARC используйте функцию [**ммиоинсталлиопрок**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="83e65-111">To install an I/O procedure associated with the .ARC filename extension, use the [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) function as follows:</span></span>


```C++
mmioInstallIOProc (mmioFOURCC('A', 'R', 'C', ' '), 
    (LPMMIOPROC)lpmmioproc, MMIO_INSTALLPROC); 
```



<span data-ttu-id="83e65-112">При установке процедуры ввода-вывода с помощью [**ммиоинсталлиопрок**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)процедура остается установленной до ее удаления.</span><span class="sxs-lookup"><span data-stu-id="83e65-112">When you install an I/O procedure using [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc), the procedure remains installed until you remove it.</span></span> <span data-ttu-id="83e65-113">Процедура ввода-вывода используется для любого открываемого файла, если файл имеет соответствующее расширение имени файла.</span><span class="sxs-lookup"><span data-stu-id="83e65-113">The I/O procedure is used for any file you open as long as the file has the appropriate filename extension.</span></span>

<span data-ttu-id="83e65-114">Также можно временно установить процедуру ввода-вывода с помощью функции [**ммиупен**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .</span><span class="sxs-lookup"><span data-stu-id="83e65-114">You can also temporarily install an I/O procedure by using the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span> <span data-ttu-id="83e65-115">В этом случае процедура ввода-вывода используется только с файлом, открытым с помощью **ммиупен** , и удаляется при закрытии файла с помощью функции [**ммиоклосе**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) .</span><span class="sxs-lookup"><span data-stu-id="83e65-115">In this case, the I/O procedure is used only with a file opened by using **mmioOpen** and is removed when the file is closed by using the [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) function.</span></span> <span data-ttu-id="83e65-116">Чтобы указать процедуру ввода-вывода при открытии файла с помощью **ммиупен**, используйте параметр *лпммиоинфо* для ссылки на структуру [**ммиоинфо**](/previous-versions//dd757322(v=vs.85)) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="83e65-116">To specify an I/O procedure when you open a file by using **mmioOpen**, use the *lpmmioinfo* parameter to reference an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure as follows:</span></span>

1.  <span data-ttu-id="83e65-117">Установите для элемента **ФкЦиопрок** **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="83e65-117">Set the **fccIOProc** member to **NULL**.</span></span>
2.  <span data-ttu-id="83e65-118">Задайте для элемента **пиопрок** адрес процедуры-экземпляра процедуры ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="83e65-118">Set the **pIOProc** member to the procedure-instance address of the I/O procedure.</span></span>
3.  <span data-ttu-id="83e65-119">Задайте для всех остальных членов значение 0 (если не открыть файл памяти или прямое чтение или запись в буфер файлового ввода-вывода).</span><span class="sxs-lookup"><span data-stu-id="83e65-119">Set all other members to zero (unless you are opening a memory file, or directly reading or writing to the file I/O buffer).</span></span>

<span data-ttu-id="83e65-120">Не забудьте удалить все установленные процедуры ввода-вывода перед выходом из приложения.</span><span class="sxs-lookup"><span data-stu-id="83e65-120">Be sure to remove any I/O procedures you have installed before you exit your application.</span></span>

 

 