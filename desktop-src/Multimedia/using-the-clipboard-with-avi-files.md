---
title: Использование буфера обмена с файлами AVI
description: Использование буфера обмена с файлами AVI
ms.assetid: 76ef7cc9-9afd-462a-b9fe-2b62f8113a9a
keywords:
- Функция Авипутфилеонклипбоард
- Функция Авижетфромклипбоард
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe46f463f22aa2d015d4ffd8496eb95c37053a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776157"
---
# <a name="using-the-clipboard-with-avi-files"></a><span data-ttu-id="e5a76-105">Использование буфера обмена с файлами AVI</span><span class="sxs-lookup"><span data-stu-id="e5a76-105">Using the Clipboard with AVI Files</span></span>

<span data-ttu-id="e5a76-106">Буфер обмена предоставляет удобное, временное хранилище, которое приложение может использовать для копирования или перемещения AVI.</span><span class="sxs-lookup"><span data-stu-id="e5a76-106">The clipboard provides convenient, temporary storage that an application can use to copy or transfer AVI files.</span></span> <span data-ttu-id="e5a76-107">Авифиле включает функции буфера обмена, которые можно использовать с дисками или файлами памяти.</span><span class="sxs-lookup"><span data-stu-id="e5a76-107">AVIFile includes clipboard functions that you can use with disk or memory files.</span></span>

<span data-ttu-id="e5a76-108">Файл можно скопировать в буфер обмена с помощью функции [**авипутфилеонклипбоард**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) .</span><span class="sxs-lookup"><span data-stu-id="e5a76-108">You can copy a file to the clipboard by using the [**AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) function.</span></span> <span data-ttu-id="e5a76-109">Чтобы записать файл из буфера обмена в память или на диск, используйте функцию [**авижетфромклипбоард**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard) .</span><span class="sxs-lookup"><span data-stu-id="e5a76-109">To write a file that is on the clipboard to memory or disk, use the [**AVIGetFromClipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard) function.</span></span>

<span data-ttu-id="e5a76-110">Вы можете очистить файл из буфера обмена с помощью функции [**авиклеарклипбоард**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) .</span><span class="sxs-lookup"><span data-stu-id="e5a76-110">You can clear a file from the clipboard by using the [**AVIClearClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) function.</span></span> <span data-ttu-id="e5a76-111">Эта функция не удаляет другие типы данных, например текст, из буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="e5a76-111">This function does not clear other types of information, such as text, from the clipboard.</span></span> <span data-ttu-id="e5a76-112">Если в приложении используются функции буфера обмена, очистите буфер обмена с **авиклеарклипбоард** перед закрытием приложения или закрытием файла в буфере обмена.</span><span class="sxs-lookup"><span data-stu-id="e5a76-112">If you use clipboard functions in your application, clear the clipboard with **AVIClearClipboard** before closing the application or closing the file on the clipboard.</span></span> <span data-ttu-id="e5a76-113">Вы можете вызвать **авиклеарклипбоард** в приложении, независимо от того, использовался ли **авипутфилеонклипбоард** .</span><span class="sxs-lookup"><span data-stu-id="e5a76-113">You can call **AVIClearClipboard** in your application whether or not **AVIPutFileOnClipboard** has been used.</span></span>

> [!Note]  
> <span data-ttu-id="e5a76-114">Если приложение копирует файл в буфер обмена, а файл содержит данные потока, которые могут измениться, можно создать файл памяти клонированных потоков с помощью функции [**авимакефилефромстреамс**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) .</span><span class="sxs-lookup"><span data-stu-id="e5a76-114">If your application copies a file to the clipboard and the file contains stream data that might change, you can create a memory file of cloned streams by using the [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) function.</span></span> <span data-ttu-id="e5a76-115">Затем можно поместить файл в буфер обмена, а затем освободить исходный файл без его аннулирования.</span><span class="sxs-lookup"><span data-stu-id="e5a76-115">You can then place the file on the clipboard and then release the original file without invalidating it.</span></span>

 

 

 




