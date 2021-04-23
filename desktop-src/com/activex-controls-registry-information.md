---
title: Сведения о реестре элементов управления ActiveX
description: Сведения о реестре элементов управления ActiveX
ms.assetid: fda5b1e6-2048-4df7-ba8f-145652e3883c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b180b327a4239b220185a9073ebc7bc0826c39
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104533524"
---
# <a name="activex-controls-registry-information"></a><span data-ttu-id="ff1fd-103">Сведения о реестре элементов управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="ff1fd-103">ActiveX Controls Registry Information</span></span>

<span data-ttu-id="ff1fd-104">Существует ряд параметров и флагов, которые используются в реестре.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-104">There are a number of registry entries and flags that are used.</span></span> <span data-ttu-id="ff1fd-105">Кроме того, элементы управления могут поддерживать категории компонентов для классификации предоставляемых ими функций.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-105">Additionally, controls can support component categories to classify the features they provide.</span></span>

<span data-ttu-id="ff1fd-106">Разделы реестра, связанные с элементами управления, отмечены звездочкой в следующем дереве:</span><span class="sxs-lookup"><span data-stu-id="ff1fd-106">Registry keys related to controls are marked with an asterisk in the following tree:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {control_CLSID}
         ProgID = <identifier>
         InprocServer32 = <filename>.dll
         *DefaultIcon = <filename>.<ext>,resourceID
         *ToolboxBitmap32 = <filename>.<ext>,resourceID
         *Control
         verb
            *n = &Properties...
         *MiscStatus = 0
         TypeLib = {object_typelibID}
         *Version = version_number
```

<span data-ttu-id="ff1fd-107">Запись **дефаултикон** используется для задания значка, отображаемого при сворачивании элемента управления в значок.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-107">The **DefaultIcon** entry is used to identify an icon to be displayed when the control is minimized to an icon.</span></span> <span data-ttu-id="ff1fd-108">Функция [**екстрактикон**](/windows/win32/api/shellapi/nf-shellapi-extracticona) используется для получения значка из. DLL или. Указанный EXE файл.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-108">The [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona) function is used to get the icon from the .DLL or .EXE file specified.</span></span>

<span data-ttu-id="ff1fd-109">Запись **ToolboxBitmap32** определяет имя модуля и идентификатор ресурса для \* точечного рисунка размером 16 15, который будет использоваться для кнопки панели инструментов или панели элементов.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-109">The **ToolboxBitmap32** entry identifies the module name and resource identifier for a 16\*15 bitmap to use for the face of a toolbar or toolbox button.</span></span> <span data-ttu-id="ff1fd-110">Стандартный размер значка Windows слишком велик для использования в этой цели.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-110">The standard Windows icon size is too large to be used for this purpose.</span></span> <span data-ttu-id="ff1fd-111">Эта запись специально поддерживает контейнеры элементов управления с режимом конструктора, в котором один выбирает элементы управления и помещает их в разрабатываемую форму.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-111">This entry specifically supports control containers that have a design mode in which one selects controls and places them on a form being designed.</span></span> <span data-ttu-id="ff1fd-112">Например, в Visual Basic значок элемента управления отображается в панели элементов Visual Basic в режиме конструктора.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-112">For example, in Visual Basic, the control's icon is displayed in the Visual Basic toolbox during design mode.</span></span>

<span data-ttu-id="ff1fd-113">Запись **элемента управления** помечает объект как элемент управления.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-113">The **Control** entry marks an object as a control.</span></span> <span data-ttu-id="ff1fd-114">Эта запись часто используется контейнерами для заполнения диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-114">This entry is often used by containers to fill in dialog boxes.</span></span> <span data-ttu-id="ff1fd-115">Контейнер использует этот подраздел, чтобы определить, следует ли включать объект в диалоговое окно, в котором отображаются элементы управления.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-115">The container uses this sub-key to determine whether to include an object in a dialog box that displays controls.</span></span>

<span data-ttu-id="ff1fd-116">**Вставляемый** вложенный ключ можно также использовать с элементами управления в зависимости от того, может ли объект работать только как внедренный объект на месте без специальных функций управления.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-116">The **Insertable** sub-key can also be used with controls, depending on whether the object can act only as an in-place embedded object with no special control features.</span></span> <span data-ttu-id="ff1fd-117">Объекты, помеченные как **вставляемые** , отображаются в диалоговом окне «Вставка объекта» своего контейнера.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-117">Objects marked with **Insertable** appear in the Insert Object dialog box of their container.</span></span> <span data-ttu-id="ff1fd-118">**Вставляемая** запись обычно означает, что элемент управления был протестирован с контейнерами, не являющимися элементом управления.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-118">The **Insertable** entry generally means that the control has been tested with non-control containers.</span></span>

<span data-ttu-id="ff1fd-119">И **вставляемые** , и вложенные ключи **элемента управления** являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-119">Both the **Insertable** and the **Control** sub-keys are optional.</span></span> <span data-ttu-id="ff1fd-120">Элемент управления может опустить **вставляемый** подраздел, если он не предназначен для работы с более старыми контейнерами, которые не понимают элементы управления.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-120">A control can omit the **Insertable** sub-key if it not designed to work with older containers that do not understand controls.</span></span> <span data-ttu-id="ff1fd-121">Элемент управления может опускать ключ **элемента управления** , если он предназначен только для работы с конкретным контейнером и поэтому не хочет вставлять его в другие контейнеры.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-121">A control can omit the **Control** key if it is only designed to work with a specific container and thus does not wish to be inserted in other containers.</span></span>

<span data-ttu-id="ff1fd-122">Элементы управления должны иметь команду Properties, \_ Свойства олеиверб, а также другие поддерживаемые команды.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-122">Controls should have a Properties verb, OLEIVERB\_PROPERTIES, along with any other verbs they support.</span></span> <span data-ttu-id="ff1fd-123">Команда Properties, а также стандартная команда ОЛЕИВЕРБ \_ PRIMARY указывает элементу управления на отображение страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-123">The Properties verb, as well as the standard verb OLEIVERB\_PRIMARY, instructs the control to display its property sheet.</span></span> <span data-ttu-id="ff1fd-124">Команда свойства отображается как элемент свойства в меню контейнера, когда элемент управления активен.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-124">The Properties verb is displayed as the Properties item on the container's menu when the control is active.</span></span> <span data-ttu-id="ff1fd-125">Таким образом, элемент управления может отображать собственную страницу свойств, что позволяет пользователю получить некоторые полезные функции, даже если контейнер не обрабатывает элементы управления.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-125">This way, the control can display its own property page allowing some useful functionality to the end user, even if the container does not handle controls.</span></span>

<span data-ttu-id="ff1fd-126">Элемент управления определяет ключ **мискстатус** , который описывает себя для потенциальных контейнеров.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-126">A control defines the **MiscStatus** key to describe itself to potential containers.</span></span> <span data-ttu-id="ff1fd-127">Биты принимают значения от [**олемиск**](/windows/win32/api/oleidl/ne-oleidl-olemisc), а элементы управления добавляют несколько значений в это перечисление.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-127">The bits take on the values from [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc), and controls add several values to this enumeration.</span></span> <span data-ttu-id="ff1fd-128">Дополнительные сведения см. в описании значений перечисления **олемиск** .</span><span class="sxs-lookup"><span data-stu-id="ff1fd-128">See the **OLEMISC** enumeration values for more information.</span></span> <span data-ttu-id="ff1fd-129">Клиент может получить эти сведения, вызвав [**иолеобжект:: жетмискстатус**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) без предварительного создания экземпляра элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-129">The client can obtain this information by calling [**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) without having to instantiate the control first.</span></span>

<span data-ttu-id="ff1fd-130">Наконец, **Version** описывает версию элемента управления, которая должна соответствовать версии библиотеки типов, связанной с этим элементом управления.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-130">Finally, **Version** describes the version of the control which should match the version of the type library associated with this control.</span></span>

<span data-ttu-id="ff1fd-131">Кроме того, в сведениях о типе элемента управления атрибут помечает запись coclass как описание элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ff1fd-131">Also in the type information for a control, the attribute control marks a coclass entry as describing a control.</span></span>

 

 