---
title: IWMPClosedCaption2 Жетсамилангид, метод
description: Метод Жетсамилангид возвращает код локали (LCID) языка, поддерживаемого текущим файлом SAMI.
ms.assetid: 41aca317-6182-47c3-8bd9-ba42b92b10f4
keywords:
- Жетсамилангид метод Windows Media Player
- Жетсамилангид метод проигрывателя Windows Media Player, интерфейс IWMPClosedCaption2
- Интерфейс IWMPClosedCaption2 Windows Media Player, метод Жетсамилангид
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb9aaebecf8e86c056fa9c91141042facc6bcc18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689325"
---
# <a name="iwmpclosedcaption2getsamilangid-method"></a><span data-ttu-id="1c0cf-106">Метод IWMPClosedCaption2:: Жетсамилангид</span><span class="sxs-lookup"><span data-stu-id="1c0cf-106">IWMPClosedCaption2::getSAMILangID method</span></span>

<span data-ttu-id="1c0cf-107">Метод **жетсамилангид** возвращает код локали (LCID) языка, поддерживаемого текущим файлом Sami.</span><span class="sxs-lookup"><span data-stu-id="1c0cf-107">The **getSAMILangID** method returns the locale identifier (LCID) of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c0cf-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c0cf-108">Syntax</span></span>


```CSharp
public System.Int32 getSAMILangID(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangID( _
  ByVal nIndex As System.Int32 _
) As System.Int32
Implements IWMPClosedCaption2.getSAMILangID
```





## <a name="parameters"></a><span data-ttu-id="1c0cf-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c0cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c0cf-110">*ниндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c0cf-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c0cf-111">Объект **System. Int32** , который является начинающимся с нуля индексом LCID для извлечения.</span><span class="sxs-lookup"><span data-stu-id="1c0cf-111">A **System.Int32** that is the zero-based index of the LCID to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c0cf-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c0cf-112">Return value</span></span>

<span data-ttu-id="1c0cf-113">Объект **System. Int32** , который является LCID языка с указанным индексом.</span><span class="sxs-lookup"><span data-stu-id="1c0cf-113">A **System.Int32** that is the LCID of the language with the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c0cf-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c0cf-114">Remarks</span></span>

<span data-ttu-id="1c0cf-115">Языки в файле SAMI индексируются в порядке, указанном в файле, начиная с нуля.</span><span class="sxs-lookup"><span data-stu-id="1c0cf-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="1c0cf-116">Этот метод возвращает значение 0, если файл цифрового мультимедиа не открыт (Аксвиндовсмедиаплайер. Опенстате равен 13).</span><span class="sxs-lookup"><span data-stu-id="1c0cf-116">This method returns 0 unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c0cf-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1c0cf-117">Requirements</span></span>



| <span data-ttu-id="1c0cf-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1c0cf-118">Requirement</span></span> | <span data-ttu-id="1c0cf-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1c0cf-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c0cf-120">Версия</span><span class="sxs-lookup"><span data-stu-id="1c0cf-120">Version</span></span><br/>   | <span data-ttu-id="1c0cf-121">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1c0cf-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1c0cf-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1c0cf-122">Namespace</span></span><br/> | <span data-ttu-id="1c0cf-123">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="1c0cf-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1c0cf-124">Сборка</span><span class="sxs-lookup"><span data-stu-id="1c0cf-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1c0cf-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1c0cf-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c0cf-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c0cf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c0cf-127">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="1c0cf-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="1c0cf-128">**Интерфейс Ивмпклоседкаптион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="1c0cf-128">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1c0cf-129">**Интерфейс IWMPClosedCaption2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="1c0cf-129">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





