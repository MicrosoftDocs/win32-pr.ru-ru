---
description: 'Метод IMpeg2PsiParser:: Жеткаунтофелементаристреамс. Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow. Это не поддерживаемый API-интерфейс DirectShow.'
ms.assetid: 19ef96a8-3d5b-4da1-8cff-d6a271ad4915
title: 'Метод IMpeg2PsiParser:: Жеткаунтофелементаристреамс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfElementaryStreams
api_type:
- COM
api_location: ''
ms.openlocfilehash: fc81c0a66751751a73a3895fd31fe8651aee8caf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089162"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a><span data-ttu-id="c2d48-104">Метод IMpeg2PsiParser:: Жеткаунтофелементаристреамс</span><span class="sxs-lookup"><span data-stu-id="c2d48-104">IMpeg2PsiParser::GetCountOfElementaryStreams method</span></span>

<span data-ttu-id="c2d48-105">Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c2d48-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="c2d48-106">Это не поддерживаемый API-интерфейс DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c2d48-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="c2d48-107">`GetCountOfElementaryStreams`Метод получает количество простейших потоков в указанной программе.</span><span class="sxs-lookup"><span data-stu-id="c2d48-107">The `GetCountOfElementaryStreams` method retrieves the number of elementary streams in a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2d48-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2d48-108">Syntax</span></span>


```C++
HRESULT GetCountOfElementaryStreams(
  [in]  WORD wProgramNumber,
  [out] WORD *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="c2d48-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2d48-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2d48-110">*впрограмнумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c2d48-110">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2d48-111">Указывает \_ поле номера программы для программы, как указано в Pat.</span><span class="sxs-lookup"><span data-stu-id="c2d48-111">Specifies the program\_number field for the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="c2d48-112">*пввал* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c2d48-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2d48-113">Указатель на переменную, которая получает количество простейших потоков в программе.</span><span class="sxs-lookup"><span data-stu-id="c2d48-113">Pointer to a variable that receives the number of elementary streams in the program.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2d48-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2d48-114">Return value</span></span>

<span data-ttu-id="c2d48-115">Метод возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c2d48-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="c2d48-116">Возможные значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c2d48-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="c2d48-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c2d48-117">Return code</span></span>                                                                          | <span data-ttu-id="c2d48-118">Описание</span><span class="sxs-lookup"><span data-stu-id="c2d48-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="c2d48-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c2d48-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c2d48-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="c2d48-120">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c2d48-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="c2d48-121">Remarks</span></span>

<span data-ttu-id="c2d48-122">Чтобы получить номер программы, используйте метод **жетрекордпрограмнумбер** .</span><span class="sxs-lookup"><span data-stu-id="c2d48-122">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2d48-123">См. также</span><span class="sxs-lookup"><span data-stu-id="c2d48-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2d48-124">**Интерфейс IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="c2d48-124">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="c2d48-125">**IMpeg2PsiParser:: Жетрекордпрограмнумбер**</span><span class="sxs-lookup"><span data-stu-id="c2d48-125">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="c2d48-126">Образец фильтра средства синтаксического анализа PSI</span><span class="sxs-lookup"><span data-stu-id="c2d48-126">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




