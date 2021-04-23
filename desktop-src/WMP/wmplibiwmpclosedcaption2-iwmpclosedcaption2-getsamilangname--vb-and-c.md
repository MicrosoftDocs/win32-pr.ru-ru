---
title: IWMPClosedCaption2 Жетсамилангнаме, метод
description: Метод Жетсамилангнаме возвращает имя языка, поддерживаемого текущим файлом SAMI.
ms.assetid: 52aaf1cc-89ef-4c4c-af43-3f88dc4a9539
keywords:
- Жетсамилангнаме метод Windows Media Player
- Жетсамилангнаме метод проигрывателя Windows Media Player, интерфейс IWMPClosedCaption2
- Интерфейс IWMPClosedCaption2 Windows Media Player, метод Жетсамилангнаме
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e50df643fdd6b665de1275873fb8de9d5d094a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689318"
---
# <a name="iwmpclosedcaption2getsamilangname-method"></a><span data-ttu-id="bf2e8-106">Метод IWMPClosedCaption2:: Жетсамилангнаме</span><span class="sxs-lookup"><span data-stu-id="bf2e8-106">IWMPClosedCaption2::getSAMILangName method</span></span>

<span data-ttu-id="bf2e8-107">Метод **жетсамилангнаме** возвращает имя языка, поддерживаемого текущим файлом Sami.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-107">The **getSAMILangName** method returns the name of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf2e8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf2e8-108">Syntax</span></span>


```CSharp
public System.String getSAMILangName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMILangName
```





## <a name="parameters"></a><span data-ttu-id="bf2e8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf2e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf2e8-110">*ниндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf2e8-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2e8-111">**Объект System. Int32** , который является начинающимся с нуля индексом имени языка для извлечения.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-111">**A System.Int32** that is the zero-based index of the language name to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf2e8-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf2e8-112">Return value</span></span>

<span data-ttu-id="bf2e8-113">**Строка System. String** , которая представляет собой имя языка, указанное в файле Sami.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-113">A **System.String** that is the name of the language as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf2e8-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf2e8-114">Remarks</span></span>

<span data-ttu-id="bf2e8-115">Языки в файле SAMI индексируются в порядке, указанном в файле, начиная с нуля.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="bf2e8-116">Этот метод возвращает строку нулевой длины (""), если файл мультимедиа не открыт (Аксвиндовсмедиаплайер. Опенстате равен 13).</span><span class="sxs-lookup"><span data-stu-id="bf2e8-116">This method returns a zero-length string ("") unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf2e8-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bf2e8-117">Requirements</span></span>



| <span data-ttu-id="bf2e8-118">Требование</span><span class="sxs-lookup"><span data-stu-id="bf2e8-118">Requirement</span></span> | <span data-ttu-id="bf2e8-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bf2e8-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf2e8-120">Версия</span><span class="sxs-lookup"><span data-stu-id="bf2e8-120">Version</span></span><br/>   | <span data-ttu-id="bf2e8-121">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="bf2e8-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="bf2e8-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bf2e8-122">Namespace</span></span><br/> | <span data-ttu-id="bf2e8-123">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="bf2e8-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="bf2e8-124">Сборка</span><span class="sxs-lookup"><span data-stu-id="bf2e8-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="bf2e8-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="bf2e8-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf2e8-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf2e8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf2e8-127">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="bf2e8-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="bf2e8-128">**Интерфейс Ивмпклоседкаптион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="bf2e8-128">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bf2e8-129">**Ивмпклоседкаптион. Самиланг (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="bf2e8-129">**IWMPClosedCaption.SAMILang (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bf2e8-130">**Интерфейс IWMPClosedCaption2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="bf2e8-130">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





