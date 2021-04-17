---
title: Добавление данных скрипта в заголовок
description: Добавление данных скрипта в заголовок
ms.assetid: 25f63d9e-c81a-4098-81d4-e848659a60e5
keywords:
- Windows Media Format SDK, добавление данных скрипта в заголовки
- Расширенный системный формат (ASF), добавление данных скрипта в заголовки
- ASF (Расширенный системный формат), добавление данных скрипта в заголовки
- скрипты, добавление данных в заголовки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8052d8a5ae04b0ea821d716bf1931352c591f892
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "105700827"
---
# <a name="to-add-script-data-to-the-header"></a><span data-ttu-id="2d8a7-107">Добавление данных скрипта в заголовок</span><span class="sxs-lookup"><span data-stu-id="2d8a7-107">To Add Script Data to the Header</span></span>

<span data-ttu-id="2d8a7-108">Команды сценария можно включить в заголовок файла ASF.</span><span class="sxs-lookup"><span data-stu-id="2d8a7-108">You can include script commands in the header of an ASF file.</span></span> <span data-ttu-id="2d8a7-109">Чтобы записать команды сценария в заголовок во время кодирования, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2d8a7-109">To write script commands to the header at the time of encoding, perform the following steps.</span></span> <span data-ttu-id="2d8a7-110">Перед вызовом [**ивмвритер:: бегинвритинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2d8a7-110">Perform these steps prior to calling [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

1.  <span data-ttu-id="2d8a7-111">Получите указатель на интерфейс **ивмхеадеринфо** , вызвав **Ивмвритер:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="2d8a7-111">Obtain a pointer to the **IWMHeaderInfo** interface by calling **IWMWriter::QueryInterface**.</span></span>
2.  <span data-ttu-id="2d8a7-112">Добавьте каждую нужную команду сценария, вызвав [**ивмхеадеринфо:: аддскрипт**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript).</span><span class="sxs-lookup"><span data-stu-id="2d8a7-112">Add each desired script command by calling [**IWMHeaderInfo::AddScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript).</span></span> <span data-ttu-id="2d8a7-113">Каждый вызов принимает две строки отдельно и время презентации для использования в качестве параметров команды.</span><span class="sxs-lookup"><span data-stu-id="2d8a7-113">Each call takes the two strings separately and the presentation time to be used for the command as parameters.</span></span>

<span data-ttu-id="2d8a7-114">Когда приложение считывает файл, ему необходимо получить все команды сценария.</span><span class="sxs-lookup"><span data-stu-id="2d8a7-114">When an application reads the file, it will need to retrieve all of the script commands.</span></span> <span data-ttu-id="2d8a7-115">Чтобы найти все команды сценария в заголовке файла, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2d8a7-115">To find all script commands in the header of a file, perform the following steps.</span></span> <span data-ttu-id="2d8a7-116">Это необходимо сделать перед запуском воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="2d8a7-116">This should be done before starting playback.</span></span>

1.  <span data-ttu-id="2d8a7-117">Получите указатель на интерфейс **ивмхеадеринфо** объекта чтения (или синхронного объекта Reader), вызвав метод **QueryInterface** другого интерфейса в объекте.</span><span class="sxs-lookup"><span data-stu-id="2d8a7-117">Obtain a pointer to the **IWMHeaderInfo** interface of the reader object (or synchronous reader object) by calling the **QueryInterface** method of another interface in the object.</span></span>
2.  <span data-ttu-id="2d8a7-118">Получение общего числа скриптов в заголовке путем вызова [**ивмхеадеринфо:: жетскрипткаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount).</span><span class="sxs-lookup"><span data-stu-id="2d8a7-118">Get the total number of scripts in the header by calling [**IWMHeaderInfo::GetScriptCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount).</span></span>
3.  <span data-ttu-id="2d8a7-119">Перебрать все скрипты в заголовке по одному за раз, используя вызовы [**ивмхеадеринфо:: надстрочный**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript).</span><span class="sxs-lookup"><span data-stu-id="2d8a7-119">Loop through all of the scripts in the header one at a time using calls to [**IWMHeaderInfo::GetScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript).</span></span>
4.  <span data-ttu-id="2d8a7-120">Создайте список времени презентации, чтобы приложение могла реагировать на команды в нужное время.</span><span class="sxs-lookup"><span data-stu-id="2d8a7-120">Create a list of the presentation times so that your application can react to the commands at the appropriate time.</span></span>

> [!Note]  
> <span data-ttu-id="2d8a7-121">При использовании DRM для шифрования файла ни одна из команд сценария не может иметь время презентации, равное 0.</span><span class="sxs-lookup"><span data-stu-id="2d8a7-121">When using DRM to encrypt a file, no script command can have a presentation time of 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2d8a7-122">См. также</span><span class="sxs-lookup"><span data-stu-id="2d8a7-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d8a7-123">**Интерфейс Ивмхеадеринфо**</span><span class="sxs-lookup"><span data-stu-id="2d8a7-123">**IWMHeaderInfo Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[<span data-ttu-id="2d8a7-124">**Интерфейс Ивмвритер**</span><span class="sxs-lookup"><span data-stu-id="2d8a7-124">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="2d8a7-125">**Использование команд сценария**</span><span class="sxs-lookup"><span data-stu-id="2d8a7-125">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




