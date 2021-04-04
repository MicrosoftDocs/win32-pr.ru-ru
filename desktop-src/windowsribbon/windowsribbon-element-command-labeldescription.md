---
title: Свойство Command. Лабелдескриптион
description: Представляет описание метки.
ms.assetid: 6c683e9e-0742-466e-9fdd-3d29f8ccb9ff
keywords:
- Лента Windows для свойства Command. Лабелдескриптион
topic_type:
- apiref
api_name:
- Command.LabelDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f748425b4c8363feee737d18c750b3a1d91121b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989204"
---
# <a name="commandlabeldescription-property"></a><span data-ttu-id="ba053-104">Свойство Command. Лабелдескриптион</span><span class="sxs-lookup"><span data-stu-id="ba053-104">Command.LabelDescription property</span></span>

<span data-ttu-id="ba053-105">Представляет описание метки.</span><span class="sxs-lookup"><span data-stu-id="ba053-105">Represents a label description.</span></span>

## <a name="usage"></a><span data-ttu-id="ba053-106">Использование</span><span class="sxs-lookup"><span data-stu-id="ba053-106">Usage</span></span>

``` syntax
<Command.LabelDescription>
  child elements
</Command.LabelDescription>
```

## <a name="attributes"></a><span data-ttu-id="ba053-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ba053-107">Attributes</span></span>

<span data-ttu-id="ba053-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="ba053-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ba053-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ba053-109">Child elements</span></span>



| <span data-ttu-id="ba053-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="ba053-110">Element</span></span>                                                   | <span data-ttu-id="ba053-111">Описание</span><span class="sxs-lookup"><span data-stu-id="ba053-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="ba053-112">**Строка**</span><span class="sxs-lookup"><span data-stu-id="ba053-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="ba053-113">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="ba053-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ba053-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ba053-114">Parent elements</span></span>



| <span data-ttu-id="ba053-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="ba053-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="ba053-116">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="ba053-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ba053-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba053-117">Remarks</span></span>

<span data-ttu-id="ba053-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="ba053-118">Optional.</span></span>

<span data-ttu-id="ba053-119">Для каждой [**команды**](windowsribbon-element-command.md)может выполняться не более одного раза.</span><span class="sxs-lookup"><span data-stu-id="ba053-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="ba053-120">**Command. лабелдескриптион** может содержать значение *типа xs: String* , ограниченное любой последовательностью символов, включая пробелы и символы разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="ba053-120">**Command.LabelDescription** can contain a value of *type xs:string* constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="ba053-121">Используйте ссылку на символ XML универсальной кодировки (UCS) `&#xA;` для указания разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="ba053-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="ba053-122">Максимальная длина не ограничена.</span><span class="sxs-lookup"><span data-stu-id="ba053-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="ba053-123">Если для **Command. лабелдескриптион** не указано значение, требуется дочерний элемент [**String**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="ba053-123">If no value is supplied for **Command.LabelDescription**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="ba053-124">Если **Command. лабелдескриптион** содержит как значение, так и дочерний элемент [**String**](windowsribbon-element-string.md) , то приоритет имеет **строка** .</span><span class="sxs-lookup"><span data-stu-id="ba053-124">If **Command.LabelDescription** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="ba053-125">**Command. лабелдескриптион** поддерживает только выравнивание по левому краю.</span><span class="sxs-lookup"><span data-stu-id="ba053-125">**Command.LabelDescription** only supports left alignment.</span></span>

## <a name="examples"></a><span data-ttu-id="ba053-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="ba053-126">Examples</span></span>

<span data-ttu-id="ba053-127">В следующем примере показан манифест команд буфера обмена с различными объявлениями **Command. лабелдескриптион** .</span><span class="sxs-lookup"><span data-stu-id="ba053-127">The following example shows a manifest of clipboard Commands with various **Command.LabelDescription** declarations.</span></span>


```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```



## <a name="requirements"></a><span data-ttu-id="ba053-128">Требования</span><span class="sxs-lookup"><span data-stu-id="ba053-128">Requirements</span></span>



| <span data-ttu-id="ba053-129">Требование</span><span class="sxs-lookup"><span data-stu-id="ba053-129">Requirement</span></span> | <span data-ttu-id="ba053-130">Значение</span><span class="sxs-lookup"><span data-stu-id="ba053-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ba053-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba053-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ba053-132">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ba053-132">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ba053-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba053-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ba053-134">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ba053-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ba053-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba053-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba053-136">UI \_ PKEY \_ лабелдескриптион</span><span class="sxs-lookup"><span data-stu-id="ba053-136">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 





