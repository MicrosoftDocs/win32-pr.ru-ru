---
description: Описывает процессы для реализации обработчиков событий устройств в реестре.
ms.assetid: 84B12B5C-C179-4124-A1FC-B90D120336BF
title: Регистрация обработчика для события устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef15071b349afa3f863e7c57b64c280c2aef8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909536"
---
# <a name="how-to-register-a-handler-for-a-device-event"></a><span data-ttu-id="94160-103">Регистрация обработчика для события устройства</span><span class="sxs-lookup"><span data-stu-id="94160-103">How to Register a Handler for a Device Event</span></span>

<span data-ttu-id="94160-104">Обработчики определяют программную часть автоматического запуска.</span><span class="sxs-lookup"><span data-stu-id="94160-104">Handlers define the software portion of AutoPlay.</span></span> <span data-ttu-id="94160-105">Они определяют значок программного обеспечения и понятное имя, а также компонент модели COM для создания экземпляра и способ инициализации компонента в ответ на событие.</span><span class="sxs-lookup"><span data-stu-id="94160-105">They define the software's icon and friendly name, as well as the Component Object Model (COM) component to instantiate and how to initialize the component in response to an event.</span></span> <span data-ttu-id="94160-106">Каждый обработчик для определенного события регистрируется как значение под соответствующим ключом **EventHandler** .</span><span class="sxs-lookup"><span data-stu-id="94160-106">Each handler for a specific event registers as a value under the appropriate **EventHandler** key.</span></span> <span data-ttu-id="94160-107">При обнаружении этого события пользователю предлагается выбрать обработчик из списка всех обработчиков, зарегистрированных для этого события.</span><span class="sxs-lookup"><span data-stu-id="94160-107">When that event is detected, the user is prompted to choose a handler from a list of all the handlers registered for that event.</span></span>

## <a name="instructions"></a><span data-ttu-id="94160-108">Инструкции</span><span class="sxs-lookup"><span data-stu-id="94160-108">Instructions</span></span>


<span data-ttu-id="94160-109">Обработчики и связанные с ними значения определяются в разделе \\ **обработчиков** аутоплайхандлерс.</span><span class="sxs-lookup"><span data-stu-id="94160-109">Handlers and their associated values are defined under the **AutoplayHandlers**\\**Handlers** key.</span></span> <span data-ttu-id="94160-110">Подразделы различаются в зависимости от того, может ли система считывать содержимое устройства напрямую или же устройство предоставляет содержимое системы через собственный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="94160-110">Subkeys differ depending on whether the system can read device contents directly or whether the device provides contents to the system through a proprietary interface.</span></span>

<span data-ttu-id="94160-111">В следующем примере показаны подразделы и значения, используемые для устройства, такие как цифровая видеокамера или MP3 Player, обеспечивающее содержимое системы через собственный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="94160-111">The following example shows the subkeys and values that are used for a device, such as a digital video camera or .mp3 player, that provides its contents to the system through a proprietary interface.</span></span> <span data-ttu-id="94160-112">Пример обработчика называется **myHandler**.</span><span class="sxs-lookup"><span data-stu-id="94160-112">The example handler is called **MyHandler**.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = Play music
                           CLSID [REG_SZ] = {a51f2ed3-634e-4a97-9d55-efcf08e7b32f}
                           DefaultIcon [REG_EXPAND_SZ] = %ProgramFiles%\Windows Media Player\wmplayer.exe,0
                           InitCmdLine [REG_SZ] = /Play
                           ProgID [REG_SZ] = WMP.PlayMusicFiles
                           Provider [REG_SZ] = Windows Media Player
```

> [!Note]  
> <span data-ttu-id="94160-113">Хотя в примере показаны как идентификатор ProgID, так и значение идентификатора класса (CLSID), на практике эти значения являются взаимоисключающими, чтобы присутствовал только один или другой.</span><span class="sxs-lookup"><span data-stu-id="94160-113">While the example shows both a ProgID and a class identifier (CLSID) value, in practice these values are mutually exclusive so that only one or the other is present.</span></span> <span data-ttu-id="94160-114">Значение ProgID является предпочтительным.</span><span class="sxs-lookup"><span data-stu-id="94160-114">The ProgID value is preferred.</span></span> <span data-ttu-id="94160-115">В зависимости от того, какой из них используется, он должен указывать на COM-компонент, реализующий интерфейс [**ихвевенсандлер**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .</span><span class="sxs-lookup"><span data-stu-id="94160-115">Whichever is used, it should point to a COM component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span>

 

<span data-ttu-id="94160-116">Значение действия можно ввести как литеральное значение, например "воспроизвести музыку", как показано в этом примере, или как имя файла со строкой ресурса.</span><span class="sxs-lookup"><span data-stu-id="94160-116">You can enter the Action value as a literal value, for example "Play music" as shown in this example, or as a file name with a resource string.</span></span> <span data-ttu-id="94160-117">Можно также ввести значение поставщика в виде литерального значения или имени файла с помощью строки ресурса.</span><span class="sxs-lookup"><span data-stu-id="94160-117">You can also enter the Provider value as a literal value or as a file name with a resource string.</span></span> <span data-ttu-id="94160-118">Автозапуск объединяет значение действия и значение поставщика со словом «using», чтобы создать дружественный заголовок, отображаемый в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="94160-118">AutoPlay combines the Action value and the Provider value with the word "using" to create a friendly caption that displays in the UI.</span></span> <span data-ttu-id="94160-119">В этом примере полученный заголовок — «воспроизводить музыку с помощью проигрывателя Windows Media».</span><span class="sxs-lookup"><span data-stu-id="94160-119">In the example, the resulting caption is "Play music using Windows Media Player."</span></span>

<span data-ttu-id="94160-120">Значение Дефаултикон указывает на ICO-файл или ресурс в двоичном файле.</span><span class="sxs-lookup"><span data-stu-id="94160-120">The DefaultIcon value points to either an .ico file or a resource in a binary file.</span></span> <span data-ttu-id="94160-121">Если числовое значение, следующее за именем двоичного файла, равно нулю или больше, то это значение индекса значка в этом двоичном файле.</span><span class="sxs-lookup"><span data-stu-id="94160-121">If the numeric value that follows the binary file name is zero or greater, then it is the index value of the icon in that binary file.</span></span> <span data-ttu-id="94160-122">Если это отрицательное значение, то это идентификатор ресурса значка.</span><span class="sxs-lookup"><span data-stu-id="94160-122">If it is a negative value, then it is the icon resource ID.</span></span> <span data-ttu-id="94160-123">Рекомендуется использовать отрицательные значения индекса.</span><span class="sxs-lookup"><span data-stu-id="94160-123">Negative index values are recommended.</span></span> <span data-ttu-id="94160-124">В случае ICO-файла значение не требуется.</span><span class="sxs-lookup"><span data-stu-id="94160-124">No value is necessary in the case of an .ico file.</span></span> <span data-ttu-id="94160-125">Рекомендуется использовать переменные среды в пути.</span><span class="sxs-lookup"><span data-stu-id="94160-125">It is recommended that you use environment variables in the path.</span></span>

<span data-ttu-id="94160-126">Значение Иниткмдлине передается без изменений с помощью метода [**ихвевенсандлер:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) перед вызовом других методов.</span><span class="sxs-lookup"><span data-stu-id="94160-126">The InitCmdLine value passes unaltered through the [**IHWEventHandler::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) method before any other methods are called.</span></span>

<span data-ttu-id="94160-127">В следующем примере показаны подразделы и значения, используемые для устройства, которое можно прочитать напрямую, например дисковод компакт-дисков или другой съемный диск.</span><span class="sxs-lookup"><span data-stu-id="94160-127">The following example shows the subkeys and values that are used for a device that can be read directly, such as a CD-ROM drive or other removable disk.</span></span> <span data-ttu-id="94160-128">Опять же, пример обработчика называется **myHandler**.</span><span class="sxs-lookup"><span data-stu-id="94160-128">Again, the example handler is called **MyHandler**.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-276
                           DefaultIcon [REG_EXPAND_SZ] = %systemroot%\System32\wiaacmgr.exe,-2
                           InvokeProgID [REG_SZ] = WIA.AutoPlayDropHandler
                           InvokeVerb [REG_SZ] = open
                           Provider [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-101
```

<span data-ttu-id="94160-129">В этом примере значения действия и поставщика отображаются в виде имени файла со строкой ресурса, а не литеральными значениями, но строки, на которые они ссылаются, используются одинаковым образом.</span><span class="sxs-lookup"><span data-stu-id="94160-129">In this example, the Action and Provider values are shown as a file name with a resource string rather than literal values, but the strings that they reference are used in the same manner.</span></span> <span data-ttu-id="94160-130">Они объединяются со словом «using», чтобы сформировать понятный заголовок, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="94160-130">They are combined with the word "using" to form a friendly caption as explained earlier.</span></span>

<span data-ttu-id="94160-131">Значения Инвокепрогид и Инвокеверб заменяют идентификаторы CLSID, Иниткмдлине и ProgID.</span><span class="sxs-lookup"><span data-stu-id="94160-131">InvokeProgID and InvokeVerb values replace CLSID, InitCmdLine, and ProgID.</span></span> <span data-ttu-id="94160-132">Значения Инвокепрогид и Инвокеверб соответствуют именам ключей, которые находятся в **\_ \_ корневом каталоге классов hKey**, как показано в следующей записи реестра.</span><span class="sxs-lookup"><span data-stu-id="94160-132">The InvokeProgID and InvokeVerb values match key names that are found under **HKEY\_CLASSES\_ROOT**, as shown in the following registry entry.</span></span> <span data-ttu-id="94160-133">Этот набор примеров ключей соответствует конкретному примеру обработчика, описанному выше.</span><span class="sxs-lookup"><span data-stu-id="94160-133">This set of example keys corresponds to the specific Handler example described earlier.</span></span>

```
HKEY_CLASSES_ROOT
   WIA.AutoplayDropHandler
      shell
         open
            DropTarget
               Clsid = {F1ABE2B5-C073-4dba-B6EB-FD7A5111DD8F}
```

<span data-ttu-id="94160-134">Функция [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) использует CLSID для реализации соответствующего приложения.</span><span class="sxs-lookup"><span data-stu-id="94160-134">The [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function uses the CLSID to implement the appropriate application.</span></span>

<span data-ttu-id="94160-135">Определив обработчик в любом из этих двух способов, необходимо зарегистрировать его для определенного события.</span><span class="sxs-lookup"><span data-stu-id="94160-135">After you define the handler in either of these two ways, you need to register it for a specific event.</span></span> <span data-ttu-id="94160-136">Это можно сделать, указав имя обработчика в качестве значения для ключа этого события в разделе **евенсандлерс**.</span><span class="sxs-lookup"><span data-stu-id="94160-136">You do this by providing the handler name as a value for that event's key under **EventHandlers**.</span></span> <span data-ttu-id="94160-137">В следующем примере показано, как зарегистрировать **myHandler** в качестве обработчика для события женерикволумеарривал.</span><span class="sxs-lookup"><span data-stu-id="94160-137">The following example shows how to register **MyHandler** as a handler for the GenericVolumeArrival event.</span></span> <span data-ttu-id="94160-138">Ему не назначено значение данных.</span><span class="sxs-lookup"><span data-stu-id="94160-138">It has no assigned data value.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        GenericVolumeArrival
                           MyHandler [REG_SZ]
```

## <a name="related-topics"></a><span data-ttu-id="94160-139">См. также</span><span class="sxs-lookup"><span data-stu-id="94160-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94160-140">**ихвевенсандлер**</span><span class="sxs-lookup"><span data-stu-id="94160-140">**IHWEventHandler**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)
</dt> <dt>

[<span data-ttu-id="94160-141">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="94160-141">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
