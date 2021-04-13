---
description: Проверяет один файл каталога, используя стандартную политику подписывания кода операционной системы, например подписывание драйверов.
ms.assetid: 1e2a18a5-506e-46a8-9309-666bec92182d
title: Функция Псетупверификаталогфиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupVerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 3de792ae6738277d2ab7cb21d8be7f4c5ecfb573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647997"
---
# <a name="psetupverifycatalogfile-function"></a><span data-ttu-id="29396-103">Функция Псетупверификаталогфиле</span><span class="sxs-lookup"><span data-stu-id="29396-103">pSetupVerifyCatalogFile function</span></span>

<span data-ttu-id="29396-104">\[Эта функция больше не поддерживается корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="29396-104">\[This function is no longer supported by Microsoft.</span></span> <span data-ttu-id="29396-105">Для INF-файла (Установка устройства) разработчики должны использовать **сетупверифинффиле**.</span><span class="sxs-lookup"><span data-stu-id="29396-105">For an INF file (device install), developers should use **SetupVerifyInfFile**.</span></span> <span data-ttu-id="29396-106">Чтобы проверить каталог, не основанный на INF, используйте **WinVerifyTrust**.\]</span><span class="sxs-lookup"><span data-stu-id="29396-106">To validate a non-INF based catalog, use **WinVerifyTrust**.\]</span></span>

<span data-ttu-id="29396-107">Проверяет один файл каталога, используя стандартную политику подписывания кода операционной системы, например подписывание драйверов.</span><span class="sxs-lookup"><span data-stu-id="29396-107">Verifies a single catalog file using standard operating system code signing policy, such as driver signing.</span></span>

## <a name="syntax"></a><span data-ttu-id="29396-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29396-108">Syntax</span></span>


```C++
DWORD pSetupVerifyCatalogFile(
  _In_ LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="29396-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="29396-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29396-110">*Каталогфуллпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="29396-110">*CatalogFullPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29396-111">Полный путь к файлу каталога, который необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="29396-111">The fully qualified path of the catalog file to be verified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29396-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="29396-112">Return value</span></span>

<span data-ttu-id="29396-113">Если функция завершается успешно, возвращается **сообщение об \_ ошибке**; в противном случае возвращается ошибка от [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span><span class="sxs-lookup"><span data-stu-id="29396-113">If the function succeeds, it returns **ERROR\_SUCCESS**; otherwise, it returns the error from [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span></span>

## <a name="remarks"></a><span data-ttu-id="29396-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29396-114">Remarks</span></span>

<span data-ttu-id="29396-115">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="29396-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="29396-116">Требования</span><span class="sxs-lookup"><span data-stu-id="29396-116">Requirements</span></span>



| <span data-ttu-id="29396-117">Требование</span><span class="sxs-lookup"><span data-stu-id="29396-117">Requirement</span></span> | <span data-ttu-id="29396-118">Значение</span><span class="sxs-lookup"><span data-stu-id="29396-118">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29396-119">DLL</span><span class="sxs-lookup"><span data-stu-id="29396-119">DLL</span></span><br/> | <dl> <span data-ttu-id="29396-120"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29396-120"><dt>Setupapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29396-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29396-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29396-122">**сетупверифинффиле**</span><span class="sxs-lookup"><span data-stu-id="29396-122">**SetupVerifyInfFile**</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupverifyinffilea)
</dt> <dt>

[<span data-ttu-id="29396-123">**WinVerifyTrust**</span><span class="sxs-lookup"><span data-stu-id="29396-123">**WinVerifyTrust**</span></span>](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)
</dt> </dl>

 

 
