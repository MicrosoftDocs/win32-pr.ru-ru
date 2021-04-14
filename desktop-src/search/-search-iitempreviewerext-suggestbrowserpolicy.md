---
description: Предлагает политику безопасности, применяемую к браузеру.
ms.assetid: 73541611-2024-4c33-ab03-e3204244c46c
title: 'Метод Иитемпревиеверекст:: Сугжестбровсерполици'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.SuggestBrowserPolicy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0a4f248edbfa4a1779016e40d73051d8c1d9acac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497073"
---
# <a name="iitempreviewerextsuggestbrowserpolicy-method"></a><span data-ttu-id="e8ac9-103">Метод Иитемпревиеверекст:: Сугжестбровсерполици</span><span class="sxs-lookup"><span data-stu-id="e8ac9-103">IItemPreviewerExt::SuggestBrowserPolicy method</span></span>

<span data-ttu-id="e8ac9-104">Предлагает политику безопасности, применяемую к браузеру.</span><span class="sxs-lookup"><span data-stu-id="e8ac9-104">Suggests the security policy to be applied to the browser.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8ac9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8ac9-105">Syntax</span></span>


```C++
HRESULT SuggestBrowserPolicy(
  [in]          DWORD dwContext,
  [out, retval] DWORD *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e8ac9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8ac9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8ac9-107">*двконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8ac9-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8ac9-108">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e8ac9-108">Type: **DWORD**</span></span>

<span data-ttu-id="e8ac9-109">Идентификатор контекста для операции.</span><span class="sxs-lookup"><span data-stu-id="e8ac9-109">The context identifier for the operation.</span></span> <span data-ttu-id="e8ac9-110">Переопределите *двконтекст* по умолчанию, чтобы задать для идентификатора контекста значение, выбранное вами.</span><span class="sxs-lookup"><span data-stu-id="e8ac9-110">Override the *dwContext* default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="e8ac9-111">*пдвфлагс* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e8ac9-111">*pdwFlags* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e8ac9-112">Введите: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="e8ac9-112">Type: \**DWORD\** _</span></span>

<span data-ttu-id="e8ac9-113">Указатель на значение DWORD, содержащее флаги проверки.</span><span class="sxs-lookup"><span data-stu-id="e8ac9-113">A pointer to a DWORD value containing verification check flags.</span></span> <span data-ttu-id="e8ac9-114">Флаг _ *бровсерполици \_ ненадежного \_ содержимого*\* отключает возможность предварительного просмотра выполнять скрипт или ActiveX.</span><span class="sxs-lookup"><span data-stu-id="e8ac9-114">The _ *BROWSERPOLICY\_UNTRUSTED\_CONTENT*\* flag disables any possibility of the preview being able to run script or ActiveX.</span></span> <span data-ttu-id="e8ac9-115">Параметр *пдвфлагс* не должен быть **пустым** указателем.</span><span class="sxs-lookup"><span data-stu-id="e8ac9-115">The parameter *pdwFlags* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8ac9-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8ac9-116">Return value</span></span>

<span data-ttu-id="e8ac9-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e8ac9-117">Type: **HRESULT**</span></span>

<span data-ttu-id="e8ac9-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e8ac9-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e8ac9-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e8ac9-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8ac9-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8ac9-120">Remarks</span></span>

<span data-ttu-id="e8ac9-121">Интерфейс [**иитемпревиеверекст**](-search-iitempreviewerext.md) поддерживается только в Windows XP и windows Server 2003 и больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="e8ac9-121">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="e8ac9-122">Для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать интерфейс [**иитемпревиеверекст**](-search-iitempreviewerext.md) и следующие API: интерфейсы [**исеарчпротоколуи**](-search-isearchprotocolui.md), [**Иитемпропертибаг**](iitempropertybag.md) и [**исеарчитем**](-search-isearchitem.md) , структура [**линкинфо**](-search-linkinfo.md) и [**перечисление**](-search-linktype.md) типов ссылок.</span><span class="sxs-lookup"><span data-stu-id="e8ac9-122">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

<span data-ttu-id="e8ac9-123">Настоятельно рекомендуется использовать флаг **\_ ненадежного \_ содержимого бровсерполици** , чтобы отключить возможность предварительного просмотра выполнять скрипт или ActiveX.</span><span class="sxs-lookup"><span data-stu-id="e8ac9-123">Using the **BROWSERPOLICY\_UNTRUSTED\_CONTENT** flag is strongly recommended to disable any possibility of the preview being able to run script or ActiveX.</span></span> <span data-ttu-id="e8ac9-124">Метод **иитемпревиеверекст:: сугжестбровсерполици** может возвращать сведения о том, является ли элемент, для которого выполняется предварительный просмотр, доверенным.</span><span class="sxs-lookup"><span data-stu-id="e8ac9-124">The **IItemPreviewerExt::SuggestBrowserPolicy** method can return information on whether the item being previewed is trusted or not.</span></span> <span data-ttu-id="e8ac9-125">Это позволит элементу управления предварительного просмотра Trident выполнять скрипт и даже элементы управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="e8ac9-125">This will allow the previewer trident control to execute script, and even ActiveX controls.</span></span> <span data-ttu-id="e8ac9-126">Поскольку предварительный просмотр часто использует временные файлы для создания предварительного просмотра, это может привести к непредвиденному выполнению сценария и кода в зоне локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="e8ac9-126">Because the previewer often uses temporary files to generate the preview, doing so can result in unexpected script and code execution in the Local Computer zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8ac9-127">Требования</span><span class="sxs-lookup"><span data-stu-id="e8ac9-127">Requirements</span></span>



| <span data-ttu-id="e8ac9-128">Требование</span><span class="sxs-lookup"><span data-stu-id="e8ac9-128">Requirement</span></span> | <span data-ttu-id="e8ac9-129">Значение</span><span class="sxs-lookup"><span data-stu-id="e8ac9-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e8ac9-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8ac9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e8ac9-131">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e8ac9-131">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e8ac9-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8ac9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e8ac9-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e8ac9-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e8ac9-134">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="e8ac9-134">Redistributable</span></span><br/>          | <span data-ttu-id="e8ac9-135">Поиск на рабочем столе Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="e8ac9-135">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="e8ac9-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8ac9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8ac9-137">**иитемпревиеверекст**</span><span class="sxs-lookup"><span data-stu-id="e8ac9-137">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




