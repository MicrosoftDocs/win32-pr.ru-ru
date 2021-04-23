---
description: Метод Аддфаундлокатион добавляет каталог в кэш каталога.
ms.assetid: 0323c4ea-2e86-433b-87d0-34d1800a5627
title: 'Метод Имедиалокатор:: Аддфаундлокатион (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.AddFoundLocation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 76d878e5b013b8c6a061d777d4ec837bca85f8e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674976"
---
# <a name="imedialocatoraddfoundlocation-method"></a><span data-ttu-id="cb2fc-103">Метод Имедиалокатор:: Аддфаундлокатион</span><span class="sxs-lookup"><span data-stu-id="cb2fc-103">IMediaLocator::AddFoundLocation method</span></span>

> [!Note]  
> <span data-ttu-id="cb2fc-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-104">\[Deprecated.</span></span> <span data-ttu-id="cb2fc-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cb2fc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cb2fc-106">`AddFoundLocation`Метод добавляет каталог в кэш каталога.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-106">The `AddFoundLocation` method adds a directory to the directory cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb2fc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb2fc-107">Syntax</span></span>


```C++
HRESULT AddFoundLocation(
   BSTR DirectoryName
);
```



## <a name="parameters"></a><span data-ttu-id="cb2fc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb2fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb2fc-109">*директоринаме*</span><span class="sxs-lookup"><span data-stu-id="cb2fc-109">*DirectoryName*</span></span> 
</dt> <dd>

<span data-ttu-id="cb2fc-110">Путь к каталогу для добавления в кэш.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-110">Directory path to add to the cache.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb2fc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb2fc-111">Return value</span></span>

<span data-ttu-id="cb2fc-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cb2fc-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cb2fc-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb2fc-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb2fc-114">Remarks</span></span>

<span data-ttu-id="cb2fc-115">Указатель мультимедиа хранит кэш путей к каталогам, в которых файлы успешно найдены в прошлых поисках.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-115">The media locator keeps a cache of directory paths where it has successfully found files in past searches.</span></span> <span data-ttu-id="cb2fc-116">После успешного нахождение файла он добавляет каталог в кэш.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-116">When it successfully locates a file, it adds the directory to the cache.</span></span>

> [!Note]  
> <span data-ttu-id="cb2fc-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cb2fc-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="cb2fc-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cb2fc-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="cb2fc-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cb2fc-120">Требования</span><span class="sxs-lookup"><span data-stu-id="cb2fc-120">Requirements</span></span>



| <span data-ttu-id="cb2fc-121">Требование</span><span class="sxs-lookup"><span data-stu-id="cb2fc-121">Requirement</span></span> | <span data-ttu-id="cb2fc-122">Значение</span><span class="sxs-lookup"><span data-stu-id="cb2fc-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb2fc-123">Header</span><span class="sxs-lookup"><span data-stu-id="cb2fc-123">Header</span></span><br/>  | <dl> <span data-ttu-id="cb2fc-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb2fc-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cb2fc-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cb2fc-125">Library</span></span><br/> | <dl> <span data-ttu-id="cb2fc-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb2fc-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb2fc-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb2fc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb2fc-128">**Интерфейс Имедиалокатор**</span><span class="sxs-lookup"><span data-stu-id="cb2fc-128">**IMediaLocator Interface**</span></span>](imedialocator.md)
</dt> <dt>

[<span data-ttu-id="cb2fc-129">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="cb2fc-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




