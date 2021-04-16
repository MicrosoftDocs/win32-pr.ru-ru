---
title: THEME. Опендиалог
description: Метод Опендиалог открывает диалоговое окно файла.
ms.assetid: d7f4549c-a5c3-4902-b13b-51f3d4444ea9
keywords:
- Проигрыватель Windows Media THEME. Опендиалог
topic_type:
- apiref
api_name:
- THEME.openDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79b9478b6b970b1d8d18b6f40975479e4755fa6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699286"
---
# <a name="themeopendialog"></a><span data-ttu-id="73003-104">THEME. Опендиалог</span><span class="sxs-lookup"><span data-stu-id="73003-104">THEME.openDialog</span></span>

<span data-ttu-id="73003-105">Метод **опендиалог** открывает диалоговое окно файла.</span><span class="sxs-lookup"><span data-stu-id="73003-105">The **openDialog** method opens a file dialog box.</span></span>

``` syntax
        theme.openDialog(dialogType, parameters)
```

## <a name="parameters"></a><span data-ttu-id="73003-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="73003-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73003-107"><span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*диалогтипе*</span><span class="sxs-lookup"><span data-stu-id="73003-107"><span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*dialogType*</span></span>
</dt> <dd>

<span data-ttu-id="73003-108">**Строка** , указывающая тип диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="73003-108">A **String** that specifies the type of dialog box.</span></span> <span data-ttu-id="73003-109">Необходимо задать значение "открыть файл \_ ".</span><span class="sxs-lookup"><span data-stu-id="73003-109">Must be set to "FILE\_OPEN".</span></span>

</dd> <dt>

<span data-ttu-id="73003-110"><span id="parameters"></span><span id="PARAMETERS"></span>*Вход*</span><span class="sxs-lookup"><span data-stu-id="73003-110"><span id="parameters"></span><span id="PARAMETERS"></span>*parameters*</span></span>
</dt> <dd>

<span data-ttu-id="73003-111">**Строка** , которую можно использовать для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="73003-111">A **String** that can be used for additional information.</span></span> <span data-ttu-id="73003-112">Необходимо задать значение FILEs \_ аллмедиа.</span><span class="sxs-lookup"><span data-stu-id="73003-112">Must be set to "FILES\_ALLMEDIA".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73003-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73003-113">Return Value</span></span>

<span data-ttu-id="73003-114">Этот метод возвращает **строку** , содержащую URL-адрес выбранного файла, или "" (пустая строка), если пользователь нажимает кнопку "Отмена".</span><span class="sxs-lookup"><span data-stu-id="73003-114">This method returns a **String** containing the URL of the selected file or "" (empty string) if the user clicks cancel.</span></span>

## <a name="remarks"></a><span data-ttu-id="73003-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73003-115">Remarks</span></span>

<span data-ttu-id="73003-116">Этот метод можно использовать для файлов на локальных жестких дисках или на сетевых дисках.</span><span class="sxs-lookup"><span data-stu-id="73003-116">This method can be used for files on the local hard drives or on network drives.</span></span>

## <a name="examples"></a><span data-ttu-id="73003-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="73003-117">Examples</span></span>


```JScript
<THEME>
  <VIEW id="View1" 
    backgroundImage="greenstone.bmp" 
    width=500 height=300 author="Microsoft Corp.">
    <BUTTON 
      id="Open" 
      image="Open.png" 
      onclick="jscript:
        player.URL = theme.openDialog('FILE_OPEN','FILES_ALLMEDIA')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="73003-118">Требования</span><span class="sxs-lookup"><span data-stu-id="73003-118">Requirements</span></span>



| <span data-ttu-id="73003-119">Требование</span><span class="sxs-lookup"><span data-stu-id="73003-119">Requirement</span></span> | <span data-ttu-id="73003-120">Значение</span><span class="sxs-lookup"><span data-stu-id="73003-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="73003-121">Версия</span><span class="sxs-lookup"><span data-stu-id="73003-121">Version</span></span><br/> | <span data-ttu-id="73003-122">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="73003-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="73003-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73003-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73003-124">**Элемент THEME**</span><span class="sxs-lookup"><span data-stu-id="73003-124">**THEME Element**</span></span>](theme-element.md)
</dt> </dl>

 

 





