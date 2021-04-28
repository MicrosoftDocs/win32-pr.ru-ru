---
description: 'Метод IMpeg2PsiParser:: Жетрекордпрограмнумбер. Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow. Это не поддерживаемый API-интерфейс DirectShow.'
ms.assetid: 3800a0b1-a581-40ed-81ab-3d5f77f442df
title: 'Метод IMpeg2PsiParser:: Жетрекордпрограмнумбер'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetRecordProgramNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0fd99178edaa23f2cdf32672a746f79c368b4265
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089142"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a><span data-ttu-id="ca5c1-104">Метод IMpeg2PsiParser:: Жетрекордпрограмнумбер</span><span class="sxs-lookup"><span data-stu-id="ca5c1-104">IMpeg2PsiParser::GetRecordProgramNumber method</span></span>

<span data-ttu-id="ca5c1-105">Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ca5c1-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="ca5c1-106">Это не поддерживаемый API-интерфейс DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ca5c1-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="ca5c1-107">`GetRecordProgramNumber`Метод извлекает номер программы для указанной программы.</span><span class="sxs-lookup"><span data-stu-id="ca5c1-107">The `GetRecordProgramNumber` method retrieves the program number for a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca5c1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca5c1-108">Syntax</span></span>


```C++
HRESULT GetRecordProgramNumber(
  [in]  DWORD dwIndex,
  [out] WORD  *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="ca5c1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca5c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca5c1-110">*двиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ca5c1-110">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca5c1-111">Указывает запись в PAT, определяющую программу, индексируемую от нуля.</span><span class="sxs-lookup"><span data-stu-id="ca5c1-111">Specifies the entry in the PAT that defines the program, indexed from zero.</span></span>

</dd> <dt>

<span data-ttu-id="ca5c1-112">*пввал* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ca5c1-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca5c1-113">Указатель на переменную, которая получает поле "номер программы" \_ из Pat.</span><span class="sxs-lookup"><span data-stu-id="ca5c1-113">Pointer to a variable that receives the program\_number field from the PAT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca5c1-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca5c1-114">Return value</span></span>

<span data-ttu-id="ca5c1-115">Метод возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ca5c1-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="ca5c1-116">Возможные значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ca5c1-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="ca5c1-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ca5c1-117">Return code</span></span>                                                                          | <span data-ttu-id="ca5c1-118">Описание</span><span class="sxs-lookup"><span data-stu-id="ca5c1-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="ca5c1-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ca5c1-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ca5c1-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="ca5c1-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="ca5c1-121">См. также</span><span class="sxs-lookup"><span data-stu-id="ca5c1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca5c1-122">**Интерфейс IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="ca5c1-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="ca5c1-123">Образец фильтра средства синтаксического анализа PSI</span><span class="sxs-lookup"><span data-stu-id="ca5c1-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




