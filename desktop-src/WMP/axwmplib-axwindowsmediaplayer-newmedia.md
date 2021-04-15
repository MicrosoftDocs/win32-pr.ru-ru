---
title: Аксвиндовсмедиаплайер. Невмедиа, метод
description: Метод Невмедиа возвращает интерфейс Ивмпмедиа для нового элемента мультимедиа.
ms.assetid: d10a517e-b4da-4f0b-9d51-9d387578d7dd
keywords:
- Невмедиа метод Windows Media Player
- Невмедиа метод Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, метод Невмедиа
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093a4e2b8181aac9148686108ad2c5c318a4d0cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695167"
---
# <a name="axwindowsmediaplayernewmedia-method"></a><span data-ttu-id="93be4-106">Аксвиндовсмедиаплайер. Невмедиа, метод</span><span class="sxs-lookup"><span data-stu-id="93be4-106">AxWindowsMediaPlayer.newMedia method</span></span>

<span data-ttu-id="93be4-107">Метод Невмедиа возвращает интерфейс Ивмпмедиа для нового элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="93be4-107">The newMedia method returns an IWMPMedia interface for a new media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="93be4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93be4-108">Syntax</span></span>


```CSharp
public IWMPMedia newMedia(
  System.String bstrURL
);
```


```VB

Public Function newMedia( _
  ByVal bstrURL As System.String _
) As IWMPMedia
```





## <a name="parameters"></a><span data-ttu-id="93be4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="93be4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93be4-110">*бструрл*</span><span class="sxs-lookup"><span data-stu-id="93be4-110">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="93be4-111">**Строка System. String** , которая является URL-адресом файла цифрового носителя, который используется для инициализации нового элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="93be4-111">A **System.String** that is the URL of the digital media file that is used to initialize the new media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93be4-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93be4-112">Return value</span></span>

<span data-ttu-id="93be4-113">Интерфейс Вмплиб. Ивмпмедиа, представляющий только что созданный элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="93be4-113">A WMPLib.IWMPMedia interface that represents the newly created media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="93be4-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93be4-114">Remarks</span></span>

<span data-ttu-id="93be4-115">Параметр *бструрл* не должен быть строкой нулевой длины ("") или значением NULL.</span><span class="sxs-lookup"><span data-stu-id="93be4-115">The *bstrURL* parameter must not be a zero-length string ("") or null.</span></span>

## <a name="requirements"></a><span data-ttu-id="93be4-116">Требования</span><span class="sxs-lookup"><span data-stu-id="93be4-116">Requirements</span></span>



| <span data-ttu-id="93be4-117">Требование</span><span class="sxs-lookup"><span data-stu-id="93be4-117">Requirement</span></span> | <span data-ttu-id="93be4-118">Значение</span><span class="sxs-lookup"><span data-stu-id="93be4-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93be4-119">Версия</span><span class="sxs-lookup"><span data-stu-id="93be4-119">Version</span></span><br/>   | <span data-ttu-id="93be4-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="93be4-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="93be4-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="93be4-121">Namespace</span></span><br/> | <span data-ttu-id="93be4-122">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="93be4-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="93be4-123">Сборка</span><span class="sxs-lookup"><span data-stu-id="93be4-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="93be4-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="93be4-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93be4-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93be4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93be4-126">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="93be4-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="93be4-127">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="93be4-127">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





