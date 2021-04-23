---
title: Пример файла SAMI
description: Пример файла SAMI
ms.assetid: 52b566f1-0d87-4bf2-87b3-3821e69a5699
keywords:
- Проигрыватель Windows Media, синхронизированный доступный медиа-обмен (SAMI)
- Объектная модель проигрывателя Windows Media, синхронизированный доступный обмен мультимедийными данными (SAMI)
- Объектная модель, синхронизированный доступный медиа-обмен (SAMI)
- Проигрыватель Windows Media Mobile, синхронизированный доступный мультимедийный обмен (SAMI)
- Элемент управления ActiveX проигрывателя Windows Media, синхронизированный доступный мультимедийный обмен (SAMI)
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, синхронизированный доступный мультимедийный обмен (SAMI)
- Элемент управления ActiveX, синхронизированный доступный медиа-обмен (SAMI)
- Синхронизированный доступный мультимедийный обмен (SAMI), файлы
- SAMI (синхронизированный доступный медиа-обмен), файлы
- Синхронизированный доступный мультимедийный обмен (SAMI), пример кода
- SAMId (синхронизированный доступный медиа-обмен), пример кода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9634de52f71b4ca1db151bdf9104c3891c8ce5d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "103914004"
---
# <a name="sami-file-example"></a><span data-ttu-id="d0f9f-114">Пример файла SAMI</span><span class="sxs-lookup"><span data-stu-id="d0f9f-114">SAMI File Example</span></span>

<span data-ttu-id="d0f9f-115">Следующий пример кода представляет собой полный файл SAMI с одним набором скрытых текста заголовка и несколькими объявлениями классов для стиля текста и языка описания.</span><span class="sxs-lookup"><span data-stu-id="d0f9f-115">The following example code is a complete SAMI file with one set of closed caption text and several class declarations for text style and caption language.</span></span>


```C++
<SAMI>
<HEAD>
   <STYLE TYPE = "text/css">
   <!--
   /* P defines the basic style selector for closed caption paragraph text */
   P {font-family:sans-serif; color:white;}
   /* Source, Small, and Big define additional ID selectors for closed caption text */
   #Source {color: orange; font-family: arial; font-size: 12pt;}
   #Small {Name: SmallTxt; font-size: 8pt; color: yellow;}
   #Big {Name: BigTxt; font-size: 12pt; color: magenta;}
   /* ENUSCC and FRFRCC define language class selectors for closed caption text */
   .ENUSCC {Name: 'English Captions'; lang: en-US; SAMIType: CC;}
   .FRFRCC {Name: 'French Captions'; lang: fr-FR; SAMIType: CC;}
   -->
   </STYLE>
</HEAD>
<BODY>
   <!<entity type="mdash"/>- The closed caption text displays at 1000 milliseconds. -->
   <SYNC Start = 1000>
      <!-- English closed captions -->
      <P Class = ENUSCC ID = Source>Narrator
      <P Class = ENUSCC>Great reason to visit Seattle, brought to you by two out-of-staters.
      <!-- French closed captions -->
      <P Class = FRFRCC ID = Source>Narrateur
      <P Class = FRFRCC>Deux personnes ne venant la r&eacute;gion vous donnent de bonnes raisons de visiter Seattle.
</BODY>
</SAMI>

```



<span data-ttu-id="d0f9f-116">Стили, определенные в файле SAMI, соответствуют стандартному синтаксису селектора CSS для элементов, классов и идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="d0f9f-116">Styles defined within a SAMI file conform to standard CSS selector syntax for elements, classes, and IDs.</span></span> <span data-ttu-id="d0f9f-117">В элементе BODY все элементы P имеют стиль, определенный для селектора элемента P в элементе STYLE.</span><span class="sxs-lookup"><span data-stu-id="d0f9f-117">In the BODY element, all P elements have the style defined for the P element selector in the STYLE element.</span></span> <span data-ttu-id="d0f9f-118">Атрибут Class элемента определяет язык элемента, определенный селекторами классов в элементе STYLE (селекторы, начинающиеся с точек).</span><span class="sxs-lookup"><span data-stu-id="d0f9f-118">The class attribute of an element specifies the language of that element as defined by the class selectors in the STYLE element (the selectors beginning with periods).</span></span> <span data-ttu-id="d0f9f-119">Имена языков, заданные селекторами класса, могут быть любой строкой.</span><span class="sxs-lookup"><span data-stu-id="d0f9f-119">The language names specified by the class selectors can be any string.</span></span> <span data-ttu-id="d0f9f-120">Для элементов с указанным атрибутом ID применяются дополнительные стили, как указано селекторами ИДЕНТИФИКАТОРов в элементе STYLE (селекторы начинаются с \# символов).</span><span class="sxs-lookup"><span data-stu-id="d0f9f-120">Elements with the ID attribute specified have additional styling applied as indicated by the ID selectors in the STYLE element (the selectors prefixed with \# characters).</span></span>

<span data-ttu-id="d0f9f-121">При использовании в сочетании с объектной моделью проигрывателя Windows Media селекторы классов соответствуют *клоседкаптион*. Свойство **самиланг** , которое можно использовать для указания языка заголовков.</span><span class="sxs-lookup"><span data-stu-id="d0f9f-121">When used in conjunction with the Windows Media Player object model, the class selectors correspond to the *ClosedCaption*.**SAMILang** property, which can be used to specify the language of the captions.</span></span> <span data-ttu-id="d0f9f-122">Селекторы ИДЕНТИФИКАТОРов соответствуют *клоседкаптион*. Свойство **самистиле** , которое можно использовать для указания стиля, в котором будут отображаться заголовки.</span><span class="sxs-lookup"><span data-stu-id="d0f9f-122">The ID selectors correspond to the *ClosedCaption*.**SAMIStyle** property, which can be used to specify the style the captions will appear in.</span></span>

<span data-ttu-id="d0f9f-123">Дополнительные сведения о создании файлов SAMI см. в статье об использовании SAMI 1,0 на [веб-сайте Майкрософт](/documentation/).</span><span class="sxs-lookup"><span data-stu-id="d0f9f-123">For more information about creating SAMI files, see Understanding SAMI 1.0 at the [Microsoft website](/documentation/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0f9f-124">См. также</span><span class="sxs-lookup"><span data-stu-id="d0f9f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0f9f-125">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="d0f9f-125">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 