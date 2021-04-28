---
description: 'Метод IMpeg2PsiParser:: Жеттранспортстреамид. Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow. Это не поддерживаемый API-интерфейс DirectShow.'
ms.assetid: 0c35abc0-984f-42df-a2a2-30cd400d4599
title: 'Метод IMpeg2PsiParser:: Жеттранспортстреамид'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetTransportStreamId
api_type:
- COM
api_location: ''
ms.openlocfilehash: a24253b021abacf398a3a169b63bbb2f01ec2354
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084572"
---
# <a name="impeg2psiparsergettransportstreamid-method"></a><span data-ttu-id="fa543-104">Метод IMpeg2PsiParser:: Жеттранспортстреамид</span><span class="sxs-lookup"><span data-stu-id="fa543-104">IMpeg2PsiParser::GetTransportStreamId method</span></span>

<span data-ttu-id="fa543-105">Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fa543-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="fa543-106">Это не поддерживаемый API-интерфейс DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fa543-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="fa543-107">`GetTransportStreamId`Метод получает поле идентификатора транспортного \_ потока \_ из Pat.</span><span class="sxs-lookup"><span data-stu-id="fa543-107">The `GetTransportStreamId` method retrieves the transport\_stream\_id field from the PAT.</span></span> <span data-ttu-id="fa543-108">Это значение определяется пользователем и может использоваться для различения определенного транспортного потока от других потоков в той же сети.</span><span class="sxs-lookup"><span data-stu-id="fa543-108">This value is defined by the user, and can be used to distinguish a particular transport stream from other streams on the same network.</span></span> <span data-ttu-id="fa543-109">Транспортный поток содержит не более одного PAT.</span><span class="sxs-lookup"><span data-stu-id="fa543-109">A transport stream contains at most one PAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa543-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa543-110">Syntax</span></span>


```C++
HRESULT GetTransportStreamId(
  [out] WORD *pStreamId
);
```



## <a name="parameters"></a><span data-ttu-id="fa543-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa543-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa543-112">*пстреамид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fa543-112">*pStreamId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa543-113">Указатель на переменную, которая получает поле идентификатора транспортного \_ потока \_ .</span><span class="sxs-lookup"><span data-stu-id="fa543-113">Pointer to a variable that receives the transport\_stream\_id field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa543-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa543-114">Return value</span></span>

<span data-ttu-id="fa543-115">Метод возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fa543-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="fa543-116">Возможные значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="fa543-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="fa543-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fa543-117">Return code</span></span>                                                                          | <span data-ttu-id="fa543-118">Описание</span><span class="sxs-lookup"><span data-stu-id="fa543-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="fa543-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fa543-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="fa543-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="fa543-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="fa543-121">См. также</span><span class="sxs-lookup"><span data-stu-id="fa543-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa543-122">**Интерфейс IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="fa543-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="fa543-123">Образец фильтра средства синтаксического анализа PSI</span><span class="sxs-lookup"><span data-stu-id="fa543-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




