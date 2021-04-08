---
title: Настройка подключаемого модуля пользовательского интерфейса
description: Настройка подключаемого модуля пользовательского интерфейса
ms.assetid: d961ed18-ba14-45af-90d3-b1e38dc53180
keywords:
- Подключаемые модули проигрывателя Windows Media, Настройка
- подключаемые модули, Настройка
- подключаемые модули пользовательского интерфейса, Настройка
- Подключаемые модули пользовательского интерфейса, Настройка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4572c4ce5102443c3100ddd20719fe17fe62ffc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068383"
---
# <a name="customizing-the-ui-plug-in"></a><span data-ttu-id="a3fab-107">Настройка подключаемого модуля пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a3fab-107">Customizing the UI Plug-in</span></span>

<span data-ttu-id="a3fab-108">На этом этапе проект готов к настройке.</span><span class="sxs-lookup"><span data-stu-id="a3fab-108">At this point, your project is ready for customization.</span></span> <span data-ttu-id="a3fab-109">Вы можете изменить созданную мастером реализацию интерфейса **ивмпплугинуи** , добавить пользовательский интерфейс в класс **кплугинвиндов** , а также реализовать страницу свойств в классе **кпропертидиалог** .</span><span class="sxs-lookup"><span data-stu-id="a3fab-109">You can modify the wizard-generated implementation of the **IWMPPluginUI** interface, you can add a user interface to the **CPluginWindow** class, and you can implement a property page in the **CPropertyDialog** class.</span></span> <span data-ttu-id="a3fab-110">Если подключаемый модуль настроен на прослушивание событий проигрывателя Windows Media, то мастер будет формировать по умолчанию или пустые реализации всех необходимых обработчиков событий, которые также будут изменены или созданы.</span><span class="sxs-lookup"><span data-stu-id="a3fab-110">If your plug-in is configured to listen to Windows Media Player events, the wizard will have generated default or empty implementations of all the necessary event handlers, which you also modify or create.</span></span>

<span data-ttu-id="a3fab-111">Тип подключаемого модуля и поддерживаемые им функции указываются значением, которое хранится в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="a3fab-111">The type of plug-in and the features it supports are indicated by a value which is stored in the Windows registry.</span></span> <span data-ttu-id="a3fab-112">Мастер создает файл с расширением RGS, который содержит сведения для регистрации подключаемого модуля с помощью.</span><span class="sxs-lookup"><span data-stu-id="a3fab-112">The wizard generates a file with a .rgs file name extension that contains the information to register the plug-in with.</span></span> <span data-ttu-id="a3fab-113">Значение "возможности" в этом файле является десятичным эквивалентом логического типа или констант типов подключаемого модуля и флагов подключаемого модуля, определенных в вмпплуг. h.</span><span class="sxs-lookup"><span data-stu-id="a3fab-113">The "Capabilities" value in this file is the decimal equivalent of a Boolean OR of the plug-in type constants and plug-in flags defined in wmpplug.h.</span></span> <span data-ttu-id="a3fab-114">Хотя это значение определяется параметрами, выбранными в мастере, его необходимо изменить, если вы хотите создать подключаемый модуль с несколькими предустановочными наборами или с помощью которых можно отправить элементы мультимедиа или списки воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="a3fab-114">Although this value is determined by the options you select in the wizard, you must modify it if you want to create a plug-in with multiple presets or one that media items or playlists can be sent to.</span></span>

<span data-ttu-id="a3fab-115">При изменении и расширении кода подключаемого модуля можно создать и зарегистрировать библиотеку DLL, чтобы можно было протестировать подключаемый модуль в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a3fab-115">As you modify and extend your plug-in code, you can build and register your DLL so that you can test your plug-in in Windows Media Player.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3fab-116">См. также</span><span class="sxs-lookup"><span data-stu-id="a3fab-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3fab-117">**Создание подключаемого модуля пользовательского интерфейса**</span><span class="sxs-lookup"><span data-stu-id="a3fab-117">**Building a UI Plug-in**</span></span>](building-a-ui-plug-in.md)
</dt> </dl>

 

 




