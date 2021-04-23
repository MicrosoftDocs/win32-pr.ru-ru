---
title: Добавление User-Controlled воспроизведения
description: Добавление User-Controlled воспроизведения
ms.assetid: c865bbc1-f78a-4d88-ab60-fba76818d175
keywords:
- Функция МЦивндкреате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198ae0bb72a5da82042b5448d2a9213358f0174d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105650278"
---
# <a name="adding-user-controlled-playback"></a><span data-ttu-id="77ef5-104">Добавление User-Controlled воспроизведения</span><span class="sxs-lookup"><span data-stu-id="77ef5-104">Adding User-Controlled Playback</span></span>

<span data-ttu-id="77ef5-105">Можно добавить управляемое пользователем воспроизведение в существующее приложение, вызвав функцию [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="77ef5-105">You can add user-controlled playback to an existing application by calling the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function as follows:</span></span>


```C++
MCIWndCreate(hwndParent, hInstModule, NULL, "filename.typ"); 
```



<span data-ttu-id="77ef5-106">Параметры [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) указывают дескрипторы родительского окна и экземпляра модуля, связанного с окном мЦивнд.</span><span class="sxs-lookup"><span data-stu-id="77ef5-106">The [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) parameters identify handles to the parent window and to the module instance associated with the MCIWnd window.</span></span> <span data-ttu-id="77ef5-107">Они также указывают стили окна и имя файла (или имя устройства), связываемые с окном МЦивнд.</span><span class="sxs-lookup"><span data-stu-id="77ef5-107">They also specify window styles and the filename (or device name) to associate with the MCIWnd window.</span></span>

<span data-ttu-id="77ef5-108">**МЦивндкреате** автоматически выполняет следующие действия, которые можно реализовать в коде для других классов окон:</span><span class="sxs-lookup"><span data-stu-id="77ef5-108">**MCIWndCreate** automatically performs the following steps that, for other window classes, you would implement in your code yourself:</span></span>

1.  <span data-ttu-id="77ef5-109">Зарегистрируйте класс окна МЦивнд.</span><span class="sxs-lookup"><span data-stu-id="77ef5-109">Register the MCIWnd window class.</span></span>
2.  <span data-ttu-id="77ef5-110">Создайте окно МЦивнд.</span><span class="sxs-lookup"><span data-stu-id="77ef5-110">Create the MCIWnd window.</span></span>
3.  <span data-ttu-id="77ef5-111">Загрузить указанное содержимое.</span><span class="sxs-lookup"><span data-stu-id="77ef5-111">Load the specified content.</span></span>
4.  <span data-ttu-id="77ef5-112">Установите текущую позиции воспроизведения в начале содержимого.</span><span class="sxs-lookup"><span data-stu-id="77ef5-112">Establish the current playback position at the beginning of the content.</span></span>
5.  <span data-ttu-id="77ef5-113">Отображение элемента управления устройством.</span><span class="sxs-lookup"><span data-stu-id="77ef5-113">Display the device control.</span></span>
6.  <span data-ttu-id="77ef5-114">При необходимости Отобразите область воспроизведения окна.</span><span class="sxs-lookup"><span data-stu-id="77ef5-114">Display the playback area of the window, if needed.</span></span>

 

 




