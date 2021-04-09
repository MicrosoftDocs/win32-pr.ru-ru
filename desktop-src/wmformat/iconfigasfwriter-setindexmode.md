---
title: Иконфигасфвритер Сетиндексмоде, метод
description: Метод Сетиндексмоде позволяет приложению контролировать, будет ли файл выполняться в течение временного индексирования.
ms.assetid: 104e29f4-a1e5-4e26-a9ef-52ef52d6f5b2
keywords:
- Формат Windows Media, Сетиндексмоде метод
- Сетиндексмоде метод Windows Media Format, интерфейс Иконфигасфвритер
- Интерфейс Иконфигасфвритер Windows Media Format, метод Сетиндексмоде
topic_type:
- apiref
api_name:
- IConfigAsfWriter.SetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25d5f2b985aeca490323aecaef2595d52b99056c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070050"
---
# <a name="iconfigasfwritersetindexmode-method"></a><span data-ttu-id="3b1e4-106">Метод Иконфигасфвритер:: Сетиндексмоде</span><span class="sxs-lookup"><span data-stu-id="3b1e4-106">IConfigAsfWriter::SetIndexMode method</span></span>

<span data-ttu-id="3b1e4-107">Метод **сетиндексмоде** позволяет приложению контролировать, будет ли файл выполняться в течение временного индексирования.</span><span class="sxs-lookup"><span data-stu-id="3b1e4-107">The **SetIndexMode** method enables the application to control whether the file will be temporally indexed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b1e4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b1e4-108">Syntax</span></span>


```C++
HRESULT SetIndexMode(
  [in] BOOL bIndexFile
);
```



## <a name="parameters"></a><span data-ttu-id="3b1e4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b1e4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b1e4-110">*биндексфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3b1e4-110">*bIndexFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b1e4-111">Переменная типа **bool**; **Значение true** указывает, что файл будет временно индексироваться.</span><span class="sxs-lookup"><span data-stu-id="3b1e4-111">Variable of type **BOOL**; **TRUE** specifies that the file will be temporally indexed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b1e4-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b1e4-112">Return value</span></span>

<span data-ttu-id="3b1e4-113">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3b1e4-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="3b1e4-114">В случае сбоя возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3b1e4-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b1e4-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b1e4-115">Remarks</span></span>

<span data-ttu-id="3b1e4-116">По умолчанию [средство записи WM ASF](wm-asf-writer-filter.md) создает файлы ASF с временным индексированием.</span><span class="sxs-lookup"><span data-stu-id="3b1e4-116">By default, the [WM ASF Writer](wm-asf-writer-filter.md) creates temporally indexed ASF files.</span></span> <span data-ttu-id="3b1e4-117">Он выполняет индексирование при остановке графа.</span><span class="sxs-lookup"><span data-stu-id="3b1e4-117">It performs the indexing when the graph stops.</span></span> <span data-ttu-id="3b1e4-118">Это поведение можно отключить, если вы хотите выполнить собственное индексирование на основе кадров в качестве этапа последующей обработки.</span><span class="sxs-lookup"><span data-stu-id="3b1e4-118">You can disable this behavior if you want to do your own frame-based indexing as a post-processing step.</span></span> <span data-ttu-id="3b1e4-119">Чтобы создать файл, индексируемый по фрейму, вызовите **сетиндексмоде**(false), создайте файл, а затем используйте методы пакета SDK Windows Media Format напрямую для создания индекса на основе фрейма для файла.</span><span class="sxs-lookup"><span data-stu-id="3b1e4-119">To create a frame-indexed file, call **SetIndexMode**(FALSE), create the file, and then use the Windows Media Format SDK methods directly to create a frame-based index for the file.</span></span>

## <a name="see-also"></a><span data-ttu-id="3b1e4-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b1e4-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="3b1e4-121">[**Интерфейс Иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3b1e4-121">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 