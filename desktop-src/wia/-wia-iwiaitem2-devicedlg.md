---
description: Отображает диалоговое окно для пользователя, чтобы подготовиться к приобретению образа.
ms.assetid: 2d7246ec-fb90-4538-b717-b9e3813c1696
title: 'IWiaItem2: метод:D Евицедлг (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3337e74a621b6431b5bbfa429692717def447c82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145421"
---
# <a name="iwiaitem2devicedlg-method"></a><span data-ttu-id="6d2fc-103">IWiaItem2: метод:D Евицедлг</span><span class="sxs-lookup"><span data-stu-id="6d2fc-103">IWiaItem2::DeviceDlg method</span></span>

<span data-ttu-id="6d2fc-104">Отображает диалоговое окно для пользователя, чтобы подготовиться к приобретению образа.</span><span class="sxs-lookup"><span data-stu-id="6d2fc-104">Displays a dialog box to the user to prepare for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d2fc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d2fc-105">Syntax</span></span>


```C++
HRESULT DeviceDlg(
  [in]      LONG      lFlags,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in, out] BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="6d2fc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d2fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d2fc-107">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d2fc-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2fc-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="6d2fc-108">Type: **LONG**</span></span>

<span data-ttu-id="6d2fc-109">Задает набор флагов, управляющих работой диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="6d2fc-109">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="6d2fc-110">Значение может быть либо 0, чтобы представлять поведение по умолчанию, либо любые \_ \_ Флаги диалогового окна WIA устройства, описанные в [**виафлаг**](-wia-wiaflag.md).</span><span class="sxs-lookup"><span data-stu-id="6d2fc-110">The value can be either 0 to represent the default behavior or any of the WIA\_DEVICE\_DIALOG flags described in [**WiaFlag**](-wia-wiaflag.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d2fc-111">*хвндпарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d2fc-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2fc-112">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="6d2fc-112">Type: **HWND**</span></span>

<span data-ttu-id="6d2fc-113">Маркер родительского окна.</span><span class="sxs-lookup"><span data-stu-id="6d2fc-113">A handle to the parent window.</span></span>

</dd> <dt>

<span data-ttu-id="6d2fc-114">*бстрфолдернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d2fc-114">*bstrFolderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2fc-115">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6d2fc-115">Type: **BSTR**</span></span>

<span data-ttu-id="6d2fc-116">Указывает имя папки, в которую будут передаваться файлы.</span><span class="sxs-lookup"><span data-stu-id="6d2fc-116">Specifies the folder name where the files are to be transferred.</span></span>

</dd> <dt>

<span data-ttu-id="6d2fc-117">*бстрфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d2fc-117">*bstrFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2fc-118">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6d2fc-118">Type: **BSTR**</span></span>

<span data-ttu-id="6d2fc-119">Указывает имя файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="6d2fc-119">Specifies the template file name.</span></span>

</dd> <dt>

<span data-ttu-id="6d2fc-120">*плнумфилес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d2fc-120">*plNumFiles* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2fc-121">Тип: \**Long \** _</span><span class="sxs-lookup"><span data-stu-id="6d2fc-121">Type: \**LONG\** _</span></span>

<span data-ttu-id="6d2fc-122">Указатель на число элементов в массиве _ppbstrFilePaths \*.</span><span class="sxs-lookup"><span data-stu-id="6d2fc-122">A pointer to the number of items in the _ppbstrFilePaths\* array.</span></span>

</dd> <dt>

<span data-ttu-id="6d2fc-123">*ппбстрфилепасс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="6d2fc-123">*ppbstrFilePaths* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2fc-124">Тип: **BSTR \* \***</span><span class="sxs-lookup"><span data-stu-id="6d2fc-124">Type: **BSTR\*\***</span></span>

<span data-ttu-id="6d2fc-125">Адрес указателя на массив путей для отсканированных файлов.</span><span class="sxs-lookup"><span data-stu-id="6d2fc-125">The address of a pointer to an array of paths for the scanned files.</span></span> <span data-ttu-id="6d2fc-126">Инициализируйте указатель, чтобы он указывал на массив нулевого размера (0) перед вызовом **IWiaItem2::D евицедлг** .</span><span class="sxs-lookup"><span data-stu-id="6d2fc-126">Initialize the pointer to point to an array of size zero (0) before **IWiaItem2::DeviceDlg** is called.</span></span>

</dd> <dt>

<span data-ttu-id="6d2fc-127">*ppIWiaItem2* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="6d2fc-127">*ppIWiaItem2* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2fc-128">Тип: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6d2fc-128">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="6d2fc-129">Адрес массива указателей на интерфейсы [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="6d2fc-129">The address of an array of pointers to [**IWiaItem2**](-wia-iwiaitem2.md) interfaces.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d2fc-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d2fc-130">Return value</span></span>

<span data-ttu-id="6d2fc-131">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6d2fc-131">Type: **HRESULT**</span></span>

<span data-ttu-id="6d2fc-132">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="6d2fc-132">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6d2fc-133">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6d2fc-133">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d2fc-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d2fc-134">Remarks</span></span>

<span data-ttu-id="6d2fc-135">Этот метод отображает диалоговое окно для пользователя, который используется приложением для сбора всех сведений, необходимых для получения образа.</span><span class="sxs-lookup"><span data-stu-id="6d2fc-135">This method displays a dialog box to the user that an application uses to gather all the information required for image acquisition.</span></span> <span data-ttu-id="6d2fc-136">Он также используется для задания свойств сканирования изображений, таких как яркость и контрастность.</span><span class="sxs-lookup"><span data-stu-id="6d2fc-136">It is also used to specify image scan properties such as brightness and contrast.</span></span>

<span data-ttu-id="6d2fc-137">После возврата этого метода приложение может использовать интерфейс [**ивиатрансфер**](-wia-iwiatransfer.md) для получения образа.</span><span class="sxs-lookup"><span data-stu-id="6d2fc-137">After this method returns, the application can use the [**IWiaTransfer**](-wia-iwiatransfer.md) interface to acquire the image.</span></span>

<span data-ttu-id="6d2fc-138">Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для каждого элемента в массиве указателей интерфейса, которые они получают с помощью параметра *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="6d2fc-138">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method for each element in the array of interface pointers they receive through the *ppIWiaItem2* parameter.</span></span> <span data-ttu-id="6d2fc-139">Приложения также должны освобождать массив с помощью [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="6d2fc-139">Applications must also free the array using [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d2fc-140">Требования</span><span class="sxs-lookup"><span data-stu-id="6d2fc-140">Requirements</span></span>



| <span data-ttu-id="6d2fc-141">Требование</span><span class="sxs-lookup"><span data-stu-id="6d2fc-141">Requirement</span></span> | <span data-ttu-id="6d2fc-142">Значение</span><span class="sxs-lookup"><span data-stu-id="6d2fc-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6d2fc-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d2fc-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6d2fc-144">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6d2fc-144">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6d2fc-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d2fc-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6d2fc-146">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6d2fc-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6d2fc-147">Header</span><span class="sxs-lookup"><span data-stu-id="6d2fc-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d2fc-148"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d2fc-148"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="6d2fc-149">IDL</span><span class="sxs-lookup"><span data-stu-id="6d2fc-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6d2fc-150"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6d2fc-150"><dt>Wia.idl</dt></span></span> </dl> |



 

 
