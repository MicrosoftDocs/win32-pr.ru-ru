---
description: Открывает журнал графики.
MS-HAID: vspixengine.IPixEngine\_OpenFile\_BSTR\_BSTR\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_LCID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипиксенгине:: OpenFile'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8E0E1336-9FC7-4C32-AF3C-F3BDF39A36D9
api_name:
- IPixEngine.OpenFile
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d18b0ff4d6d2301c6d52d2bc855d48a3db124ccb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139878"
---
# <a name="span-idvspixengineipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcidspanipixengineopenfile-method"></a><span data-ttu-id="4e6fe-103"><span id="vspixengine.ipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcid"></span>Метод Ипиксенгине:: OpenFile</span><span class="sxs-lookup"><span data-stu-id="4e6fe-103"><span id="vspixengine.ipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcid"></span>IPixEngine::OpenFile method</span></span>

<span data-ttu-id="4e6fe-104">Открывает журнал графики.</span><span class="sxs-lookup"><span data-stu-id="4e6fe-104">Opens a graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e6fe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e6fe-105">Syntax</span></span>


```C++
HRESULT OpenFile(
   BSTR                FileName,
   BSTR                registryBoot,
   INewFramesCallback* callbacks,
   IFileIOCallback*    pFileIOCallback,
   LCID                uiLocale
);
```

## <a name="parameters"></a><span data-ttu-id="4e6fe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e6fe-106">Parameters</span></span>

<span data-ttu-id="4e6fe-107">*Файлов* </span><span class="sxs-lookup"><span data-stu-id="4e6fe-107">*FileName* </span></span>  
<span data-ttu-id="4e6fe-108">Строка COM, содержащая имя журнала графики.</span><span class="sxs-lookup"><span data-stu-id="4e6fe-108">A COM string containing the name of the graphics log.</span></span>

<span data-ttu-id="4e6fe-109">*регистрибут* </span><span class="sxs-lookup"><span data-stu-id="4e6fe-109">*registryBoot* </span></span>  
<span data-ttu-id="4e6fe-110">Строка COM, содержащая корень реестра.</span><span class="sxs-lookup"><span data-stu-id="4e6fe-110">A COM string containing the registry root.</span></span> <span data-ttu-id="4e6fe-111">Обработчик ищет DIA и другие разделы реестра.</span><span class="sxs-lookup"><span data-stu-id="4e6fe-111">The engine looks here for DIA and other registry keys.</span></span>

<span data-ttu-id="4e6fe-112">*обратные вызовы* </span><span class="sxs-lookup"><span data-stu-id="4e6fe-112">*callbacks* </span></span>  
<span data-ttu-id="4e6fe-113">Адрес функции, используемой для уведомления узла о том, что были проанализированы новые кадры.</span><span class="sxs-lookup"><span data-stu-id="4e6fe-113">The address of a function used to notify the host that new frames have been parsed.</span></span>

<span data-ttu-id="4e6fe-114">*пфилеиокаллбакк* </span><span class="sxs-lookup"><span data-stu-id="4e6fe-114">*pFileIOCallback* </span></span>  
<span data-ttu-id="4e6fe-115">Адрес функции, используемой для уведомления узла об ошибках ввода-вывода в файле во время синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="4e6fe-115">The address of a function used to notify the host of file IO errors during parsing.</span></span>

<span data-ttu-id="4e6fe-116">*уилокале* </span><span class="sxs-lookup"><span data-stu-id="4e6fe-116">*uiLocale* </span></span>  
<span data-ttu-id="4e6fe-117">КОД локали, используемый для отображения сообщений об ошибках в соответствии с настройками языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="4e6fe-117">The locale ID used to present error messages according to locale settings.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e6fe-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e6fe-118">Return value</span></span>

<span data-ttu-id="4e6fe-119">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4e6fe-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4e6fe-120">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4e6fe-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e6fe-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4e6fe-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4e6fe-122">Header</span><span class="sxs-lookup"><span data-stu-id="4e6fe-122">Header</span></span></p></td><td><span data-ttu-id="4e6fe-123">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="4e6fe-123">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="4e6fe-124"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="4e6fe-124"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="4e6fe-125">**ипиксенгине**</span><span class="sxs-lookup"><span data-stu-id="4e6fe-125">**IPixEngine**</span></span>](/windows/desktop/direct3dtools/ipixengine)

 

 
