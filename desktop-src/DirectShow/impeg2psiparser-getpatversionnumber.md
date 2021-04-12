---
description: Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow. Это не поддерживаемый API-интерфейс DirectShow.
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
ms.openlocfilehash: 6117060cf0c8d3c56d03e5838376485244fde8d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416532"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a><span data-ttu-id="b8339-104">Метод IMpeg2PsiParser:: Жетпатверсионнумбер</span><span class="sxs-lookup"><span data-stu-id="b8339-104">IMpeg2PsiParser::GetPatVersionNumber method</span></span>

<span data-ttu-id="b8339-105">Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b8339-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="b8339-106">Это не поддерживаемый API-интерфейс DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b8339-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="b8339-107">`GetPatVersionNumber`Метод извлекает \_ поле номера версии из Pat.</span><span class="sxs-lookup"><span data-stu-id="b8339-107">The `GetPatVersionNumber` method retrieves the version\_number field from the PAT.</span></span> <span data-ttu-id="b8339-108">Транспортный поток содержит не более одного PAT.</span><span class="sxs-lookup"><span data-stu-id="b8339-108">A transport stream contains at most one PAT.</span></span> <span data-ttu-id="b8339-109">Номер версии увеличивается каждый раз, когда изменяется информация в таблице.</span><span class="sxs-lookup"><span data-stu-id="b8339-109">The version number is incremented whenever the information in the table changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8339-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8339-110">Syntax</span></span>


```C++
HRESULT GetPatVersionNumber(
  [out] BYTE *pPatVersion
);
```



## <a name="parameters"></a><span data-ttu-id="b8339-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8339-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8339-112">*ппатверсион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b8339-112">*pPatVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8339-113">Указатель на переменную, которая получает \_ поле номера версии.</span><span class="sxs-lookup"><span data-stu-id="b8339-113">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8339-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8339-114">Return value</span></span>

<span data-ttu-id="b8339-115">Метод возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b8339-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="b8339-116">Возможные значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b8339-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="b8339-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b8339-117">Return code</span></span>                                                                          | <span data-ttu-id="b8339-118">Описание</span><span class="sxs-lookup"><span data-stu-id="b8339-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="b8339-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b8339-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b8339-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="b8339-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="b8339-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8339-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8339-122">**Интерфейс IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="b8339-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="b8339-123">Образец фильтра средства синтаксического анализа PSI</span><span class="sxs-lookup"><span data-stu-id="b8339-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




