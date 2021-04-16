---
title: Подключаемые модули источника
description: Подключаемые модули источника
ms.assetid: 9adc2d42-6273-4af0-b57f-2dde5738ed94
keywords:
- Пакет SDK для формата Windows Media, подключаемые модули источников
- Расширенный формат систем (ASF), подключаемые модули источников
- ASF (Расширенный системный формат), подключаемые модули источников
- подключаемые модули источника
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4822b9110def4e1b758be40310f503fd56a251fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105719105"
---
# <a name="source-plug-ins"></a><span data-ttu-id="541f8-107">Подключаемые модули источника</span><span class="sxs-lookup"><span data-stu-id="541f8-107">Source Plug-ins</span></span>

<span data-ttu-id="541f8-108">Подключаемый модуль источника — это вариант, доступный разработчикам, желающим реализовать собственную систему хранения для файлов Windows Media®.</span><span class="sxs-lookup"><span data-stu-id="541f8-108">A source plug-in is an option available to developers who wish to implement their own storage system for Windows Media® files.</span></span> <span data-ttu-id="541f8-109">Подключаемый модуль источника обеспечивает это посредством реализации интерфейса COM с именем **IStream**, который является стандартным интерфейсом для предоставления данных.</span><span class="sxs-lookup"><span data-stu-id="541f8-109">A source plug-in enables this through the implementation of a COM interface called **IStream**, which is a standard interface for providing data.</span></span>

<span data-ttu-id="541f8-110">Подключаемый модуль источника должен быть написан в виде библиотеки DLL, а его присутствие известно пакету SDK с помощью записи реестра.</span><span class="sxs-lookup"><span data-stu-id="541f8-110">The source plug-in should be written as a dll, and its presence is made known to the SDK through a registry entry.</span></span> <span data-ttu-id="541f8-111">Таким способом может быть любое количество подключаемых модулей источника.</span><span class="sxs-lookup"><span data-stu-id="541f8-111">There can be any number of source plug-ins implemented this way.</span></span> <span data-ttu-id="541f8-112">Подключаемый модуль источника должен экспортировать функцию [**вмкреатестреамфорурл**](wmcreatestreamforurl.md) .</span><span class="sxs-lookup"><span data-stu-id="541f8-112">The source plug-in must export the [**WMCreateStreamForURL**](wmcreatestreamforurl.md) function.</span></span>

<span data-ttu-id="541f8-113">Чтобы зарегистрировать подключаемый модуль источника, необходимо добавить следующую запись реестра:</span><span class="sxs-lookup"><span data-stu-id="541f8-113">To register a source plug-in, the following registry entry should be added:</span></span>

<span data-ttu-id="541f8-114">HKEY \_ локальный \_ компьютер \\ программное обеспечение \\ Microsoft \\ Windows Media \\ вмсдк \\ источники</span><span class="sxs-lookup"><span data-stu-id="541f8-114">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Media\\WMSDK\\sources</span></span>

<span data-ttu-id="541f8-115">Name = "любое уникальное имя"</span><span class="sxs-lookup"><span data-stu-id="541f8-115">Name = "any unique name"</span></span>

<span data-ttu-id="541f8-116">Значение = путь к библиотеке DLL подключаемого модуля источника</span><span class="sxs-lookup"><span data-stu-id="541f8-116">Value = pathname of the source plug-in dll</span></span>

<span data-ttu-id="541f8-117">После регистрации библиотеки DLL приложение может использовать метод **ивмреадер:: Open** (с соответствующим URL-адресом в качестве параметра) для доступа к данным потока, которые могут храниться в файлах или определяемых пользователем контейнерах данных.</span><span class="sxs-lookup"><span data-stu-id="541f8-117">Once the dll has been registered, the application can use the **IWMReader::Open** method (with the appropriate URL as a parameter) to access stream data, which can be stored in files or user-defined data containers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="541f8-118">См. также</span><span class="sxs-lookup"><span data-stu-id="541f8-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="541f8-119">**Ивмреадер:: Open**</span><span class="sxs-lookup"><span data-stu-id="541f8-119">**IWMReader::Open**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)
</dt> <dt>

[<span data-ttu-id="541f8-120">**Справочник по программированию**</span><span class="sxs-lookup"><span data-stu-id="541f8-120">**Programming Reference**</span></span>](programming-reference.md)
</dt> <dt>

[<span data-ttu-id="541f8-121">**вмкреатестреамфорурл**</span><span class="sxs-lookup"><span data-stu-id="541f8-121">**WMCreateStreamForURL**</span></span>](wmcreatestreamforurl.md)
</dt> </dl>

 

 




