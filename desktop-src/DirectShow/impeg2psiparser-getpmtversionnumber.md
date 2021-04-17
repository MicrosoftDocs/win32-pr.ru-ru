---
description: Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow. Это не поддерживаемый API-интерфейс DirectShow.
ms.assetid: 50113d6b-4e10-4dc9-aaef-f67c6918a2de
title: 'Метод IMpeg2PsiParser:: Жетпмтверсионнумбер'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPmtVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3af4b20067af52216181848f4cc63ac5a7784ba9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672975"
---
# <a name="impeg2psiparsergetpmtversionnumber-method"></a><span data-ttu-id="91b2a-104">Метод IMpeg2PsiParser:: Жетпмтверсионнумбер</span><span class="sxs-lookup"><span data-stu-id="91b2a-104">IMpeg2PsiParser::GetPmtVersionNumber method</span></span>

<span data-ttu-id="91b2a-105">Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow.</span><span class="sxs-lookup"><span data-stu-id="91b2a-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="91b2a-106">Это не поддерживаемый API-интерфейс DirectShow.</span><span class="sxs-lookup"><span data-stu-id="91b2a-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="91b2a-107">`GetPmtVersionNumber`Метод извлекает \_ поле номера версии из УКАЗАННОГО типа ПЛТ.</span><span class="sxs-lookup"><span data-stu-id="91b2a-107">The `GetPmtVersionNumber` method retrieves the version\_number field from a specified PMT.</span></span> <span data-ttu-id="91b2a-108">Номер версии увеличивается при каждом изменении определения программы.</span><span class="sxs-lookup"><span data-stu-id="91b2a-108">The version number is incremented whenever the definition of the program changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="91b2a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91b2a-109">Syntax</span></span>


```C++
HRESULT GetPmtVersionNumber(
  [in]  WORD wProgramNumber,
  [out] BYTE *pPmtVersion
);
```



## <a name="parameters"></a><span data-ttu-id="91b2a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="91b2a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91b2a-111">*впрограмнумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="91b2a-111">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91b2a-112">Указывает \_ поле номера программы программы, как указано в Pat.</span><span class="sxs-lookup"><span data-stu-id="91b2a-112">Specifies the program\_number field of the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="91b2a-113">*ппмтверсион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="91b2a-113">*pPmtVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91b2a-114">Указатель на переменную, которая получает \_ поле номера версии.</span><span class="sxs-lookup"><span data-stu-id="91b2a-114">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91b2a-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91b2a-115">Return value</span></span>

<span data-ttu-id="91b2a-116">Метод возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="91b2a-116">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="91b2a-117">Возможные значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="91b2a-117">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="91b2a-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="91b2a-118">Return code</span></span>                                                                          | <span data-ttu-id="91b2a-119">Описание</span><span class="sxs-lookup"><span data-stu-id="91b2a-119">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="91b2a-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="91b2a-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="91b2a-121">Успешно.</span><span class="sxs-lookup"><span data-stu-id="91b2a-121">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="91b2a-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91b2a-122">Remarks</span></span>

<span data-ttu-id="91b2a-123">Чтобы получить номер программы, используйте метод **жетрекордпрограмнумбер** .</span><span class="sxs-lookup"><span data-stu-id="91b2a-123">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="91b2a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91b2a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91b2a-125">**Интерфейс IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="91b2a-125">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="91b2a-126">**IMpeg2PsiParser:: Жетрекордпрограмнумбер**</span><span class="sxs-lookup"><span data-stu-id="91b2a-126">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="91b2a-127">Образец фильтра средства синтаксического анализа PSI</span><span class="sxs-lookup"><span data-stu-id="91b2a-127">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




