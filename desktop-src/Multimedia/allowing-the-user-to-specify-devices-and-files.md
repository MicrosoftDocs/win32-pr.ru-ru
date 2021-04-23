---
title: Разрешение пользователю указывать устройства и файлы
description: Разрешение пользователю указывать устройства и файлы
ms.assetid: cc542b56-c66e-4622-b2d1-505d31aab25b
keywords:
- Макрос МЦивндопендиалог
- Макрос МЦивндопен
- Макрос МЦивндопенинтерфаце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4191f18409a1fb1f23ba3a2128b4aaed1b30e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776520"
---
# <a name="allowing-the-user-to-specify-devices-and-files"></a><span data-ttu-id="82951-106">Разрешение пользователю указывать устройства и файлы</span><span class="sxs-lookup"><span data-stu-id="82951-106">Allowing the User to Specify Devices and Files</span></span>

<span data-ttu-id="82951-107">Вы можете связать устройство или файл с существующим окном МЦивнд с помощью макросов [**мЦивндопендиалог**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog), [**мЦивндопен**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)и [**мЦивндопенинтерфаце**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) и функции [**жетопенфиленамепревиев**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) .</span><span class="sxs-lookup"><span data-stu-id="82951-107">You can associate a device or file with an existing MCIWnd window by using the [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog), [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen), and [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) macros, and the [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) function.</span></span>

<span data-ttu-id="82951-108">Чтобы пользователь приложения мог выбрать файл для воспроизведения, используйте **мЦивндопендиалог**.</span><span class="sxs-lookup"><span data-stu-id="82951-108">To let a user of your application select a file to play, use **MCIWndOpenDialog**.</span></span> <span data-ttu-id="82951-109">Этот макрос открывает диалоговое окно **Открыть** (как показано на следующем снимке экрана) для выбора файла и связывания выбранного файла с текущим окном мЦивнд.</span><span class="sxs-lookup"><span data-stu-id="82951-109">This macro displays the **Open** dialog box (shown in the following screen shot) for choosing a file and associates the selected file with the current MCIWnd window.</span></span>

![изображение окна мЦивнд](images/mciwnd3.gif)

<span data-ttu-id="82951-111">Можно разрешить пользователю приложения выбрать файл для связывания с окном МЦивнд и просмотреть этот файл с помощью [**жетопенфиленамепревиев**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) и [**мЦивндопен**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen).</span><span class="sxs-lookup"><span data-stu-id="82951-111">You can let a user of your application select a file to associate with an MCIWnd window and preview that file by using [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) and [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen).</span></span> <span data-ttu-id="82951-112">Функция **жетопенфиленамепревиев** отображает диалоговое окно **Открыть** для выбора файла и позволяет пользователю просмотреть его содержимое.</span><span class="sxs-lookup"><span data-stu-id="82951-112">The **GetOpenFileNamePreview** function displays the **Open** dialog box for choosing a file and lets the user preview (play) its contents.</span></span> <span data-ttu-id="82951-113">Если имя существующего файла указано в диалоговом окне, **жетопенфиленамепревиев** предоставляет небольшой элемент управления, позволяющий пользователю просмотреть содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="82951-113">When the name of an existing file is specified in the dialog box, **GetOpenFileNamePreview** provides a small control to let the user preview the contents of the file.</span></span> <span data-ttu-id="82951-114">Вы можете связать указанный файл, выбранный с **жетопенфиленамепревиев** или указанным другим способом, с окном мЦивнд с помощью **мЦивндопен**.</span><span class="sxs-lookup"><span data-stu-id="82951-114">You can associate a specified file, selected with **GetOpenFileNamePreview** or specified in another manner, with an MCIWnd window by using **MCIWndOpen**.</span></span>

<span data-ttu-id="82951-115">Можно также использовать **мЦивндопен** , чтобы указать устройство, связываемое с окном мЦивнд.</span><span class="sxs-lookup"><span data-stu-id="82951-115">You can also use **MCIWndOpen** to specify a device to associate with an MCIWnd window.</span></span> <span data-ttu-id="82951-116">Например, можно использовать имя устройства, например "Кдаудио".</span><span class="sxs-lookup"><span data-stu-id="82951-116">For example, you can use a device name, such as "CDAudio".</span></span>

<span data-ttu-id="82951-117">Чтобы связать окно МЦивнд с файловым интерфейсом или интерфейсом потока данных для мультимедийных данных, используйте макрос [**мЦивндопенинтерфаце**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) .</span><span class="sxs-lookup"><span data-stu-id="82951-117">To associate an MCIWnd window with a file interface or data-stream interface to multimedia data, use the [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) macro.</span></span> <span data-ttu-id="82951-118">Дополнительные сведения о интерфейсах файлов и потоков данных см. в разделе [Авифиле functions and Macros](avifile-functions-and-macros.md).</span><span class="sxs-lookup"><span data-stu-id="82951-118">For more information about file and data-stream interfaces, see [AVIFile Functions and Macros](avifile-functions-and-macros.md).</span></span>

> [!Note]  
> <span data-ttu-id="82951-119">Перед связыванием нового файла или устройства с окном МЦивнд [**мЦивндопендиалог**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) и [**мЦивндопен**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) закрывают все устройства, которые в настоящее время связаны с окном.</span><span class="sxs-lookup"><span data-stu-id="82951-119">Before associating a new file or device with an MCIWnd window, [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) and [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) close any device currently associated with the window.</span></span> <span data-ttu-id="82951-120">Приложению не нужно закрывать открытые устройства перед использованием этих макросов.</span><span class="sxs-lookup"><span data-stu-id="82951-120">Your application does not need to close any open devices before using these macros.</span></span>

 

 

 




