---
description: Загружает текстуру из файла и уведомляет узел асинхронно по завершении.
MS-HAID: vspixengine.IPixEngine5\_LoadTextureFromFileAsync\_BSTR\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine5:: Лоадтекстурефромфилеасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DF10C209-B6B5-4692-81D7-7FD59CE49F56
api_name:
- IPixEngine5.LoadTextureFromFileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bef4e4e5117680f7c18f13cc99f801c8e8b8bdfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140571"
---
# <a name="span-idvspixengineipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadtexturefromfileasync-method"></a><span data-ttu-id="5f971-103"><span id="vspixengine.ipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Метод IPixEngine5:: Лоадтекстурефромфилеасинк</span><span class="sxs-lookup"><span data-stu-id="5f971-103"><span id="vspixengine.ipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::LoadTextureFromFileAsync method</span></span>

<span data-ttu-id="5f971-104">Загружает текстуру из файла и уведомляет узел асинхронно по завершении.</span><span class="sxs-lookup"><span data-stu-id="5f971-104">Loads a texture from a file and notifies the host asynchronously when it completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f971-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f971-105">Syntax</span></span>


```C++
HRESULT LoadTextureFromFileAsync(
   BSTR                  fileName,
   BSTR                  histogramDataFileName,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="5f971-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f971-106">Parameters</span></span>

<span data-ttu-id="5f971-107">*Файлов* </span><span class="sxs-lookup"><span data-stu-id="5f971-107">*fileName* </span></span>  
<span data-ttu-id="5f971-108">Строка COM, содержащая имя файла текстуры.</span><span class="sxs-lookup"><span data-stu-id="5f971-108">A COM string containing the name of the texture file.</span></span>

<span data-ttu-id="5f971-109">*хистограмдатафиленаме* </span><span class="sxs-lookup"><span data-stu-id="5f971-109">*histogramDataFileName* </span></span>  
<span data-ttu-id="5f971-110">Строка COM, содержащая имя файла данных гистограммы, связанного с текстурой.</span><span class="sxs-lookup"><span data-stu-id="5f971-110">A COM string containing the name of the histogram data file associated with the texture.</span></span>

<span data-ttu-id="5f971-111">*обратные вызовы* </span><span class="sxs-lookup"><span data-stu-id="5f971-111">*callbacks* </span></span>  
<span data-ttu-id="5f971-112">Адрес объекта, который предоставляет интерфейс обратных вызовов IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="5f971-112">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="5f971-113">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="5f971-113">*requestCookie* </span></span>  
<span data-ttu-id="5f971-114">Файл cookie, который уникально иденфиес запрос, и может использоваться для оповещения об отмене.</span><span class="sxs-lookup"><span data-stu-id="5f971-114">A cookie that uniquely idenfies the request, and can be used to signal for it to be canceled.</span></span>

<span data-ttu-id="5f971-115">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="5f971-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="5f971-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="5f971-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f971-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f971-117">Return value</span></span>

<span data-ttu-id="5f971-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5f971-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5f971-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5f971-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f971-120">Требования</span><span class="sxs-lookup"><span data-stu-id="5f971-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5f971-121">Header</span><span class="sxs-lookup"><span data-stu-id="5f971-121">Header</span></span></p></td><td><span data-ttu-id="5f971-122">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="5f971-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5f971-123"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="5f971-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5f971-124">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="5f971-124">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
