---
description: 'Метод IMpeg2PsiParser:: Жеткаунтофпрограмс. Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow. Это не поддерживаемый API-интерфейс DirectShow.'
ms.assetid: 282dd779-9aca-46e3-a791-cb9ea86f637d
title: 'Метод IMpeg2PsiParser:: Жеткаунтофпрограмс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfPrograms
api_type:
- COM
api_location: ''
ms.openlocfilehash: d6bfe698a45ea1cfe0a4bac6e65b839292bc1996
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119432"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a><span data-ttu-id="9512e-104">Метод IMpeg2PsiParser:: Жеткаунтофпрограмс</span><span class="sxs-lookup"><span data-stu-id="9512e-104">IMpeg2PsiParser::GetCountOfPrograms method</span></span>

<span data-ttu-id="9512e-105">Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9512e-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="9512e-106">Это не поддерживаемый API-интерфейс DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9512e-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="9512e-107">`GetCountOfPrograms`Метод извлекает количество программ в транспортном потоке.</span><span class="sxs-lookup"><span data-stu-id="9512e-107">The `GetCountOfPrograms` method retrieves the number of programs in the transport stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="9512e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9512e-108">Syntax</span></span>


```C++
HRESULT GetCountOfPrograms(
  [out] int *pNumOfPrograms
);
```



## <a name="parameters"></a><span data-ttu-id="9512e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9512e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9512e-110">*пнумофпрограмс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9512e-110">*pNumOfPrograms* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9512e-111">Указатель на переменную, которая получает количество программ.</span><span class="sxs-lookup"><span data-stu-id="9512e-111">Pointer to a variable that receives the number of programs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9512e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9512e-112">Return value</span></span>

<span data-ttu-id="9512e-113">Метод возвращает значение HRESULT.</span><span class="sxs-lookup"><span data-stu-id="9512e-113">The method returns an HRESULT value.</span></span> <span data-ttu-id="9512e-114">Возможные значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="9512e-114">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="9512e-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9512e-115">Return code</span></span>                                                                          | <span data-ttu-id="9512e-116">Описание</span><span class="sxs-lookup"><span data-stu-id="9512e-116">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="9512e-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9512e-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9512e-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="9512e-118">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="9512e-119">См. также</span><span class="sxs-lookup"><span data-stu-id="9512e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9512e-120">**Интерфейс IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="9512e-120">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="9512e-121">Образец фильтра средства синтаксического анализа PSI</span><span class="sxs-lookup"><span data-stu-id="9512e-121">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




