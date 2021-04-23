---
description: Проверяет один файл каталога.
ms.assetid: 4b2de733-ef95-4b0a-8f53-7bc73ffaa2c2
title: Функция Верификаталогфиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 52083b23041f7f21aa51e326bc00d4cabc76eca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647933"
---
# <a name="verifycatalogfile-function"></a><span data-ttu-id="f23f1-103">Функция Верификаталогфиле</span><span class="sxs-lookup"><span data-stu-id="f23f1-103">VerifyCatalogFile function</span></span>

<span data-ttu-id="f23f1-104">\[Эта функция не поддерживается и не должна использоваться.\]</span><span class="sxs-lookup"><span data-stu-id="f23f1-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="f23f1-105">Проверяет один файл каталога.</span><span class="sxs-lookup"><span data-stu-id="f23f1-105">Verifies a single catalog file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f23f1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f23f1-106">Syntax</span></span>


```C++
DWORD VerifyCatalogFile(
   LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="f23f1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f23f1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f23f1-108">*каталогфуллпас*</span><span class="sxs-lookup"><span data-stu-id="f23f1-108">*CatalogFullPath*</span></span> 
</dt> <dd>

<span data-ttu-id="f23f1-109">Полный путь к файлу каталога, который необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="f23f1-109">The fully qualified path of the catalog file to be verified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f23f1-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f23f1-110">Return value</span></span>

<span data-ttu-id="f23f1-111">Если функция завершается успешно, возвращается **сообщение об \_ ошибке**; в противном случае возвращается ошибка от [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span><span class="sxs-lookup"><span data-stu-id="f23f1-111">If the function succeeds, it returns **ERROR\_SUCCESS**; otherwise, it returns the error from [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span></span>

<span data-ttu-id="f23f1-112">Если каталог является каталогом с подписью Authenticode, эта функция возвращает **сообщение об ошибке \_ \_ доверенный \_ Издатель Authenticode** , если он завершается. в противном случае возвращается **сообщение об ошибке " \_ \_ доверие Authenticode \_ не \_ установлено**".</span><span class="sxs-lookup"><span data-stu-id="f23f1-112">If the catalog is an Authenticode-signed catalog, this function returns **ERROR\_AUTHENTICODE\_TRUSTED\_PUBLISHER** if it succeeds; otherwise, it returns **ERROR\_AUTHENTICODE\_TRUST\_NOT\_ESTABLISHED**.</span></span>

<span data-ttu-id="f23f1-113">Если функция не может определить, является ли издатель доверенной, он также может возвращать **ошибку \_ неопознанные \_** ошибки.</span><span class="sxs-lookup"><span data-stu-id="f23f1-113">If the function is unable to determine whether the publisher is trusted, it may also return **ERROR\_UNIDENTIFIED\_ERROR**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f23f1-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f23f1-114">Remarks</span></span>

<span data-ttu-id="f23f1-115">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="f23f1-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f23f1-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f23f1-116">Requirements</span></span>



| <span data-ttu-id="f23f1-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f23f1-117">Requirement</span></span> | <span data-ttu-id="f23f1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f23f1-118">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f23f1-119">DLL</span><span class="sxs-lookup"><span data-stu-id="f23f1-119">DLL</span></span><br/> | <dl> <span data-ttu-id="f23f1-120"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f23f1-120"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
