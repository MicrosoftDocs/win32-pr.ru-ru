---
title: Иконфигасфвритер Жетиндексмоде, метод
description: Метод Жетиндексмоде извлекает текущий режим временного индекса.
ms.assetid: beb874ea-d0d5-4323-a817-47984911da4c
keywords:
- Формат Windows Media, Жетиндексмоде метод
- Жетиндексмоде метод Windows Media Format, интерфейс Иконфигасфвритер
- Интерфейс Иконфигасфвритер Windows Media Format, метод Жетиндексмоде
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb701f591579d3113e79b0b9b74167ac8de3d75f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413217"
---
# <a name="iconfigasfwritergetindexmode-method"></a><span data-ttu-id="5da1e-106">Метод Иконфигасфвритер:: Жетиндексмоде</span><span class="sxs-lookup"><span data-stu-id="5da1e-106">IConfigAsfWriter::GetIndexMode method</span></span>

<span data-ttu-id="5da1e-107">Метод **жетиндексмоде** извлекает текущий режим временного индекса.</span><span class="sxs-lookup"><span data-stu-id="5da1e-107">The **GetIndexMode** method retrieves the current temporal index mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="5da1e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5da1e-108">Syntax</span></span>


```C++
HRESULT GetIndexMode(
  [out] BOOL *pbIndexFile
);
```



## <a name="parameters"></a><span data-ttu-id="5da1e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5da1e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5da1e-110">*пбиндексфиле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5da1e-110">*pbIndexFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5da1e-111">Указатель на переменную типа **bool** , которая получает параметр режима временных индексов.</span><span class="sxs-lookup"><span data-stu-id="5da1e-111">Pointer to a variable of type **BOOL** that receives the temporal index mode setting.</span></span> <span data-ttu-id="5da1e-112">Значение **true** указывает, что модуль записи WM ASF настроен для записи временных индексированных файлов.</span><span class="sxs-lookup"><span data-stu-id="5da1e-112">A value of **TRUE** indicates that the WM ASF Writer is configured to write temporally indexed files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5da1e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5da1e-113">Return value</span></span>

<span data-ttu-id="5da1e-114">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="5da1e-114">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="5da1e-115">В случае сбоя возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5da1e-115">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5da1e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5da1e-116">Remarks</span></span>

<span data-ttu-id="5da1e-117">Используйте этот метод, чтобы определить, настроен ли [модуль записи WM ASF](wm-asf-writer-filter.md) для записи файлов ASF с временным индексированием.</span><span class="sxs-lookup"><span data-stu-id="5da1e-117">Use this method to determine whether the [WM ASF Writer](wm-asf-writer-filter.md) is currently configured to write temporally indexed ASF files.</span></span> <span data-ttu-id="5da1e-118">Дополнительные сведения о временных индексированных и индексированных файлах см. в разделе Примечания для [**иконфигасфвритер:: сетиндексмоде**](iconfigasfwriter-setindexmode.md).</span><span class="sxs-lookup"><span data-stu-id="5da1e-118">For more information on temporally indexed and frame-indexed files, see the Remarks for [**IConfigAsfWriter::SetIndexMode**](iconfigasfwriter-setindexmode.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5da1e-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5da1e-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="5da1e-120">[**Интерфейс Иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5da1e-120">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 