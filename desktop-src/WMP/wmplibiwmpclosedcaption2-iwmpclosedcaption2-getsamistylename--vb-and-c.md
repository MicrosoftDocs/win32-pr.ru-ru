---
title: IWMPClosedCaption2 Жетсамистиленаме, метод
description: Метод Жетсамистиленаме возвращает имя стиля, поддерживаемого текущим файлом SAMI.
ms.assetid: e7678ca6-f52f-45f4-bd1c-7fbcdf1cc47c
keywords:
- Жетсамистиленаме метод Windows Media Player
- Жетсамистиленаме метод проигрывателя Windows Media Player, интерфейс IWMPClosedCaption2
- Интерфейс IWMPClosedCaption2 Windows Media Player, метод Жетсамистиленаме
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMIStyleName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ceb3f598ae603d478af5cad9c78333952530a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689317"
---
# <a name="iwmpclosedcaption2getsamistylename-method"></a><span data-ttu-id="2b339-106">Метод IWMPClosedCaption2:: Жетсамистиленаме</span><span class="sxs-lookup"><span data-stu-id="2b339-106">IWMPClosedCaption2::getSAMIStyleName method</span></span>

<span data-ttu-id="2b339-107">Метод **жетсамистиленаме** возвращает имя стиля, поддерживаемого текущим файлом Sami.</span><span class="sxs-lookup"><span data-stu-id="2b339-107">The **getSAMIStyleName** method returns the name of a style supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b339-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b339-108">Syntax</span></span>


```CSharp
public System.String getSAMIStyleName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMIStyleName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMIStyleName
```





## <a name="parameters"></a><span data-ttu-id="2b339-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b339-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b339-110">*ниндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b339-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b339-111">Объект **System. Int32** , который является начинающимся с нуля индексом имени стиля для извлечения.</span><span class="sxs-lookup"><span data-stu-id="2b339-111">A **System.Int32** that is the zero-based index of the style name to retrieve</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b339-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b339-112">Return value</span></span>

<span data-ttu-id="2b339-113">**Строка System. String** , которая является именем стиля, как указано в файле Sami.</span><span class="sxs-lookup"><span data-stu-id="2b339-113">A **System.String** that is the name of the style as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b339-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b339-114">Remarks</span></span>

<span data-ttu-id="2b339-115">Стили в файле SAMI индексируются в порядке, указанном в файле, начиная с нуля.</span><span class="sxs-lookup"><span data-stu-id="2b339-115">The styles in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="2b339-116">Этот метод возвращает строку нулевой длины (""), если файл мультимедиа не открыт (Аксвиндовсмедиаплайер. Опенстате равен 13).</span><span class="sxs-lookup"><span data-stu-id="2b339-116">This method returns a zero-length string ("") unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b339-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2b339-117">Requirements</span></span>



| <span data-ttu-id="2b339-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2b339-118">Requirement</span></span> | <span data-ttu-id="2b339-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2b339-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b339-120">Версия</span><span class="sxs-lookup"><span data-stu-id="2b339-120">Version</span></span><br/>   | <span data-ttu-id="2b339-121">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2b339-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2b339-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2b339-122">Namespace</span></span><br/> | <span data-ttu-id="2b339-123">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="2b339-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2b339-124">Сборка</span><span class="sxs-lookup"><span data-stu-id="2b339-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2b339-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2b339-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b339-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b339-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b339-127">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="2b339-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="2b339-128">**Интерфейс Ивмпклоседкаптион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2b339-128">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2b339-129">**Ивмпклоседкаптион. Самистиле (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2b339-129">**IWMPClosedCaption.SAMIStyle (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2b339-130">**Интерфейс IWMPClosedCaption2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2b339-130">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





