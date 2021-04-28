---
description: 'Метод IMpeg2PsiParser:: Жетпатверсионнумбер. Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow. Это не поддерживаемый API-интерфейс DirectShow.'
ms.assetid: 2f5ad9bf-3d70-491a-ab45-15cd922a02d4
title: 'Метод IMpeg2PsiParser:: Жетпатверсионнумбер'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPatVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 978da4c7076bcf8ffe91bc2b9a4b2077d9d3d48a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089152"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a><span data-ttu-id="acd3e-104">Метод IMpeg2PsiParser:: Жетпатверсионнумбер</span><span class="sxs-lookup"><span data-stu-id="acd3e-104">IMpeg2PsiParser::GetPatVersionNumber method</span></span>

<span data-ttu-id="acd3e-105">Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow.</span><span class="sxs-lookup"><span data-stu-id="acd3e-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="acd3e-106">Это не поддерживаемый API-интерфейс DirectShow.</span><span class="sxs-lookup"><span data-stu-id="acd3e-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="acd3e-107">`GetPatVersionNumber`Метод извлекает \_ поле номера версии из Pat.</span><span class="sxs-lookup"><span data-stu-id="acd3e-107">The `GetPatVersionNumber` method retrieves the version\_number field from the PAT.</span></span> <span data-ttu-id="acd3e-108">Транспортный поток содержит не более одного PAT.</span><span class="sxs-lookup"><span data-stu-id="acd3e-108">A transport stream contains at most one PAT.</span></span> <span data-ttu-id="acd3e-109">Номер версии увеличивается каждый раз, когда изменяется информация в таблице.</span><span class="sxs-lookup"><span data-stu-id="acd3e-109">The version number is incremented whenever the information in the table changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="acd3e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="acd3e-110">Syntax</span></span>


```C++
HRESULT GetPatVersionNumber(
  [out] BYTE *pPatVersion
);
```



## <a name="parameters"></a><span data-ttu-id="acd3e-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="acd3e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acd3e-112">*ппатверсион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="acd3e-112">*pPatVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acd3e-113">Указатель на переменную, которая получает \_ поле номера версии.</span><span class="sxs-lookup"><span data-stu-id="acd3e-113">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acd3e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="acd3e-114">Return value</span></span>

<span data-ttu-id="acd3e-115">Метод возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="acd3e-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="acd3e-116">Возможные значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="acd3e-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="acd3e-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="acd3e-117">Return code</span></span>                                                                          | <span data-ttu-id="acd3e-118">Описание</span><span class="sxs-lookup"><span data-stu-id="acd3e-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="acd3e-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="acd3e-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="acd3e-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="acd3e-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="acd3e-121">См. также</span><span class="sxs-lookup"><span data-stu-id="acd3e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acd3e-122">**Интерфейс IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="acd3e-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="acd3e-123">Образец фильтра средства синтаксического анализа PSI</span><span class="sxs-lookup"><span data-stu-id="acd3e-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




