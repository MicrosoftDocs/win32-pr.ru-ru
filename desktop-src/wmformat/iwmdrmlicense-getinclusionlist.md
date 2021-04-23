---
title: Метод Ивмдрмлиценсе Жетинклусионлист (Вмдрмсдк. h)
description: Метод Жетинклусионлист извлекает весь список включения для текущей лицензии или цепочки лицензий.
ms.assetid: a3cb70c5-7d20-413c-aeb8-66c9233b384e
keywords:
- Формат Windows Media, Жетинклусионлист метод
- Жетинклусионлист метод Windows Media Format, интерфейс Ивмдрмлиценсе
- Интерфейс Ивмдрмлиценсе Windows Media Format, метод Жетинклусионлист
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetInclusionList
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f0d2837a4bb84c07214cce3e4fbc3d4d96b9583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704073"
---
# <a name="iwmdrmlicensegetinclusionlist-method"></a><span data-ttu-id="c876d-106">Метод Ивмдрмлиценсе:: Жетинклусионлист</span><span class="sxs-lookup"><span data-stu-id="c876d-106">IWMDRMLicense::GetInclusionList method</span></span>

<span data-ttu-id="c876d-107">Метод **жетинклусионлист** извлекает весь список включения для текущей лицензии или цепочки лицензий.</span><span class="sxs-lookup"><span data-stu-id="c876d-107">The **GetInclusionList** method retrieves the entire inclusion list for the current license or license chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="c876d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c876d-108">Syntax</span></span>


```C++
HRESULT GetInclusionList(
  [out] GUID  **ppGuids,
  [out] DWORD *pcGuids
);
```



## <a name="parameters"></a><span data-ttu-id="c876d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c876d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c876d-110">*ппгуидс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c876d-110">*ppGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c876d-111">Получает массив идентификаторов GUID, определяющих включаемые технологии.</span><span class="sxs-lookup"><span data-stu-id="c876d-111">Receives an array of GUIDs identifying the included technologies.</span></span>

</dd> <dt>

<span data-ttu-id="c876d-112">*пкгуидс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c876d-112">*pcGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c876d-113">Получает количество элементов в массиве *ппгуидс* .</span><span class="sxs-lookup"><span data-stu-id="c876d-113">Receives the number of elements in the *ppGuids* array.</span></span> <span data-ttu-id="c876d-114">Массив выделяется с помощью функции **CoTaskMemAlloc**.</span><span class="sxs-lookup"><span data-stu-id="c876d-114">The array is allocated by using **CoTaskMemAlloc**.</span></span> <span data-ttu-id="c876d-115">После завершения работы со списком освободите память, вызвав **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="c876d-115">When finished with the list, release the memory by calling **CoTaskMemFree**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c876d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c876d-116">Return value</span></span>

<span data-ttu-id="c876d-117">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c876d-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c876d-118">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c876d-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c876d-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c876d-119">Return code</span></span>                                                                          | <span data-ttu-id="c876d-120">Описание</span><span class="sxs-lookup"><span data-stu-id="c876d-120">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c876d-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c876d-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c876d-122">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="c876d-122">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c876d-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c876d-123">Remarks</span></span>

<span data-ttu-id="c876d-124">Издатель лицензии может указывать другие системы защиты, для которых может быть преобразовано зашифрованное содержимое.</span><span class="sxs-lookup"><span data-stu-id="c876d-124">The license issuer can specify other protection systems to which the encrypted content may be converted.</span></span> <span data-ttu-id="c876d-125">Список идентификаторов GUID, полученных этим методом, определяет разрешенные системы защиты.</span><span class="sxs-lookup"><span data-stu-id="c876d-125">The list of GUIDs retrieved by this method identifies the allowed protection systems.</span></span> <span data-ttu-id="c876d-126">При вводе в лицензионное соглашение с корпорацией Майкрософт для получения библиотеки-заглушки вы получите список поддерживаемых в настоящее время систем защиты и идентификаторы GUID, используемые для их обнаружения.</span><span class="sxs-lookup"><span data-stu-id="c876d-126">When you enter into a license agreement with Microsoft to get the stub library, you will receive a list of currently supported protection systems and the GUIDs used to identify them.</span></span>

## <a name="requirements"></a><span data-ttu-id="c876d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="c876d-127">Requirements</span></span>



| <span data-ttu-id="c876d-128">Требование</span><span class="sxs-lookup"><span data-stu-id="c876d-128">Requirement</span></span> | <span data-ttu-id="c876d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="c876d-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c876d-130">Header</span><span class="sxs-lookup"><span data-stu-id="c876d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c876d-131"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="c876d-131"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="c876d-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c876d-132">Library</span></span><br/> | <dl> <span data-ttu-id="c876d-133"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c876d-133"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c876d-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c876d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c876d-135">**Явные списки авторизации и включений**</span><span class="sxs-lookup"><span data-stu-id="c876d-135">**Explicit Authorization and Inclusion Lists**</span></span>](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[<span data-ttu-id="c876d-136">**Интерфейс Ивмдрмлиценсе**</span><span class="sxs-lookup"><span data-stu-id="c876d-136">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





