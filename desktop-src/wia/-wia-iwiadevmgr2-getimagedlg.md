---
description: 'Метод IWiaDevMgr2:: Жетимажедлг отображает одно или несколько диалоговых окон, которые позволяют пользователю получить изображение с устройства Windows (WIA) 2,0 и записать образ в указанный файл.'
ms.assetid: 30a63426-150e-44cf-a03e-7b6da14450f7
title: 'Метод IWiaDevMgr2:: Жетимажедлг (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.GetImageDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6777b839beeb809383e524960e8882392be4bd24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719515"
---
# <a name="iwiadevmgr2getimagedlg-method"></a><span data-ttu-id="75206-103">Метод IWiaDevMgr2:: Жетимажедлг</span><span class="sxs-lookup"><span data-stu-id="75206-103">IWiaDevMgr2::GetImageDlg method</span></span>

<span data-ttu-id="75206-104">Метод **IWiaDevMgr2:: жетимажедлг** отображает одно или несколько диалоговых окон, которые позволяют пользователю получить изображение с устройства Windows (WIA) 2,0 и записать образ в указанный файл.</span><span class="sxs-lookup"><span data-stu-id="75206-104">The **IWiaDevMgr2::GetImageDlg** method displays one or more dialog boxes that enable a user to acquire an image from a Windows Image Acquisition (WIA) 2.0 device and write the image to a specified file.</span></span> <span data-ttu-id="75206-105">Этот метод расширяет функциональные возможности [**IWiaDevMgr2:: селектдевицедлг**](-wia-iwiadevmgr2-selectdevicedlg.md) для инкапсуляции получения образа в рамках одного вызова API.</span><span class="sxs-lookup"><span data-stu-id="75206-105">This method extends the functionality of [**IWiaDevMgr2::SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) to encapsulate image acquisition within a single API call.</span></span>

## <a name="syntax"></a><span data-ttu-id="75206-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75206-106">Syntax</span></span>


```C++
HRESULT GetImageDlg(
  [in]      LONG      lFlags,
  [in]      BSTR      bstrDeviceID,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in]      BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppItem
);
```



## <a name="parameters"></a><span data-ttu-id="75206-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="75206-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75206-108">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="75206-108">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75206-109">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="75206-109">Type: **LONG**</span></span>

<span data-ttu-id="75206-110">Задает поведение диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="75206-110">Specifies dialog box behavior.</span></span> <span data-ttu-id="75206-111">Можно задать следующие значения:</span><span class="sxs-lookup"><span data-stu-id="75206-111">Can be set to the following values:</span></span>



| <span data-ttu-id="75206-112">Flag</span><span class="sxs-lookup"><span data-stu-id="75206-112">Flag</span></span>                                 | <span data-ttu-id="75206-113">Значение</span><span class="sxs-lookup"><span data-stu-id="75206-113">Meaning</span></span>                                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75206-114">0</span><span class="sxs-lookup"><span data-stu-id="75206-114">0</span></span>                                    | <span data-ttu-id="75206-115">Поведение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="75206-115">Default behavior.</span></span>                                                                                                                                                           |
| <span data-ttu-id="75206-116">\_ \_ \_ \_ Общий \_ Пользовательский интерфейс диалогового окна устройства WIA</span><span class="sxs-lookup"><span data-stu-id="75206-116">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="75206-117">Используйте пользовательский интерфейс системы вместо пользовательского интерфейса, предоставленного поставщиком.</span><span class="sxs-lookup"><span data-stu-id="75206-117">Use the system UI instead of the vendor-supplied UI.</span></span> <span data-ttu-id="75206-118">Если пользовательский интерфейс системы недоступен, используется пользовательский интерфейс поставщика.</span><span class="sxs-lookup"><span data-stu-id="75206-118">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="75206-119">Если ни один из ИНТЕРФЕЙСов не доступен, функция возвращает E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="75206-119">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="75206-120">*бстрдевицеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="75206-120">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75206-121">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="75206-121">Type: **BSTR**</span></span>

<span data-ttu-id="75206-122">Указывает используемый сканер.</span><span class="sxs-lookup"><span data-stu-id="75206-122">Specifies the scanner to use.</span></span>

</dd> <dt>

<span data-ttu-id="75206-123">*хвндпарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="75206-123">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75206-124">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="75206-124">Type: **HWND**</span></span>

<span data-ttu-id="75206-125">Маркер окна, которому принадлежит диалоговое окно " **Получение изображения** ".</span><span class="sxs-lookup"><span data-stu-id="75206-125">A handle of the window that owns the **Get Image** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="75206-126">*бстрфолдернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="75206-126">*bstrFolderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75206-127">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="75206-127">Type: **BSTR**</span></span>

<span data-ttu-id="75206-128">Указывает имя папки, в которую загруженного хранить сканированные файлы.</span><span class="sxs-lookup"><span data-stu-id="75206-128">Specifies the name of the folder ito store the scanned files in.</span></span>

</dd> <dt>

<span data-ttu-id="75206-129">*бстрфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="75206-129">*bstrFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75206-130">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="75206-130">Type: **BSTR**</span></span>

<span data-ttu-id="75206-131">Указывает имя файла, в который записываются данные изображения.</span><span class="sxs-lookup"><span data-stu-id="75206-131">Specifies the name of the file to write the image data to.</span></span>

</dd> <dt>

<span data-ttu-id="75206-132">*плнумфилес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="75206-132">*plNumFiles* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75206-133">Тип: \**Long \** _</span><span class="sxs-lookup"><span data-stu-id="75206-133">Type: \**LONG\** _</span></span>

<span data-ttu-id="75206-134">Указатель на число проверяемых файлов.</span><span class="sxs-lookup"><span data-stu-id="75206-134">A pointer to the number of files to scan.</span></span>

</dd> <dt>

<span data-ttu-id="75206-135">_ppbstrFilePaths \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="75206-135">_ppbstrFilePaths\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75206-136">Тип: **BSTR \* \***</span><span class="sxs-lookup"><span data-stu-id="75206-136">Type: **BSTR\*\***</span></span>

<span data-ttu-id="75206-137">Адрес указателя на массив путей для отсканированных файлов.</span><span class="sxs-lookup"><span data-stu-id="75206-137">The address of a pointer to an array of paths for the scanned files.</span></span> <span data-ttu-id="75206-138">Инициализируйте указатель, чтобы он указывал на массив нулевого размера (0) перед вызовом **IWiaDevMgr2:: жетимажедлг** .</span><span class="sxs-lookup"><span data-stu-id="75206-138">Initialize the pointer to point to an array of size zero (0) before **IWiaDevMgr2::GetImageDlg** is called.</span></span> <span data-ttu-id="75206-139">См. **Примечания**.</span><span class="sxs-lookup"><span data-stu-id="75206-139">See **Remarks**.</span></span>

</dd> <dt>

<span data-ttu-id="75206-140">*ппитем* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="75206-140">*ppItem* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="75206-141">Тип: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="75206-141">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="75206-142">Адрес указателя на [**IWiaItem2**](-wia-iwiaitem2.md) , из которого были проверены изображения.</span><span class="sxs-lookup"><span data-stu-id="75206-142">The address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) that the images were scanned from.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75206-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75206-143">Return value</span></span>

<span data-ttu-id="75206-144">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="75206-144">Type: **HRESULT**</span></span>

<span data-ttu-id="75206-145">**IWiaDevMgr2:: жетимажедлг** возвращает \_ ОК, если данные успешно передаются, возвращает \_ значение s false, если пользователь отменяет диалоговое окно, или ВОЗВРАЩАЕТ стандартную ошибку com.</span><span class="sxs-lookup"><span data-stu-id="75206-145">**IWiaDevMgr2::GetImageDlg** returns S\_OK if the data is transferred successfully, returns S\_FALSE if the user cancels the dialog box, or returns a standard COM error.</span></span>

> [!Note]  
> <span data-ttu-id="75206-146">Параметр *ппбстрфилепасс* не обязательно должен быть пустым, если функция возвращает \_ значение false.</span><span class="sxs-lookup"><span data-stu-id="75206-146">The *ppbstrFilePaths* parameter is not necessarily empty, if the function returns S\_FALSE.</span></span> <span data-ttu-id="75206-147">Если пользователь отменяет действие, страницы с завершенным сканированием обрабатываются и возвращаются в *ппбстрфилепасс*.</span><span class="sxs-lookup"><span data-stu-id="75206-147">If the user cancels, the pages that have completed scanning are processed and returned in *ppbstrFilePaths*.</span></span> <span data-ttu-id="75206-148">Даже если они не используются, необходимо освободить массив.</span><span class="sxs-lookup"><span data-stu-id="75206-148">Even if they are not used, you must free the array.</span></span> <span data-ttu-id="75206-149">См. **Примечания**.</span><span class="sxs-lookup"><span data-stu-id="75206-149">See **Remarks**.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="75206-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="75206-150">Remarks</span></span>

<span data-ttu-id="75206-151">Если приложение передает значение **null** в качестве значения параметра *бстрдевицеид* , **IWiaDevMgr2:: Жетимажедлг** отображает диалоговое окно **Выбор устройства** , чтобы пользователь мог выбрать устройство для ввода данных WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="75206-151">If the application passes **NULL** for the value of the *bstrDeviceID* parameter, **IWiaDevMgr2::GetImageDlg** displays the **Select Device** dialog box so that the user can select the WIA 2.0 input device.</span></span>

<span data-ttu-id="75206-152">Используйте пункт меню **из сканера** в меню **файл** , чтобы параметры устройства и изображения были доступны в приложении.</span><span class="sxs-lookup"><span data-stu-id="75206-152">Use a menu item named **From scanner** on the **File** menu so that device and image selections are available in your application.</span></span>

<span data-ttu-id="75206-153">Вызовите [сисфристринг](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) для каждого BSTR в массиве, на который указывает *ппбстрфилепасс* \[ \] , и вызовите [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) в самом массиве, чтобы освободить связанную память.</span><span class="sxs-lookup"><span data-stu-id="75206-153">Call [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) on each BSTR in the array that *ppbstrFilePaths*\[i\] points to, and call [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) on the array itself to free associated memory.</span></span> <span data-ttu-id="75206-154">Если \_ возвращается значение S false, проверьте, не равны ли значения, которые *плнумфилес* указывает, на ноль.</span><span class="sxs-lookup"><span data-stu-id="75206-154">If S\_FALSE is returned, check to see if the value that *plNumFiles* points to is not zero.</span></span> <span data-ttu-id="75206-155">Если значение не равно нулю, освободите ресурсы *ппбстрфилепасс* \[ i \] в приложении, так как пользователь может отменить сканирование одной или нескольких страниц.</span><span class="sxs-lookup"><span data-stu-id="75206-155">If the value is not zero, free the *ppbstrFilePaths*\[i\] resources in the application, because the user might cancel after scanning one or more pages.</span></span> <span data-ttu-id="75206-156">Инициализируйте *плнумфилес* до нуля перед вызовом **IWiaDevMgr2:: жетимажедлг**.</span><span class="sxs-lookup"><span data-stu-id="75206-156">Initialize *plNumFiles* to zero before you call **IWiaDevMgr2::GetImageDlg**.</span></span> <span data-ttu-id="75206-157">Если *плнумфилес* не инициализировано равным нулю и ошибка в инфраструктуре com приводит к тому, что функция возвращает значение \_ false, прежде чем **IWiaDevMgr2:: жетимажедлг** , то *плнумфилес* будет иметь неверное значение сборки мусора.</span><span class="sxs-lookup"><span data-stu-id="75206-157">If *plNumFiles* is not initialized to zero and a failure in the COM infrastructure causes the function to return S\_FALSE before **IWiaDevMgr2::GetImageDlg** is called, then *plNumFiles* will have a misleading garbage value.</span></span>

<span data-ttu-id="75206-158">Диалоговое окно должно иметь достаточные права для *бстрфолдернаме* , чтобы можно было сохранить файлы с уникальными именами файлов.</span><span class="sxs-lookup"><span data-stu-id="75206-158">The dialog box must have sufficient rights to *bstrFolderName* so that it can save the files with unique file names.</span></span> <span data-ttu-id="75206-159">Защитите папку с помощью списка управления доступом (ACL), так как он содержит пользовательские данные.</span><span class="sxs-lookup"><span data-stu-id="75206-159">Protect the folder with an access control list (ACL) because it contains user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="75206-160">Требования</span><span class="sxs-lookup"><span data-stu-id="75206-160">Requirements</span></span>



| <span data-ttu-id="75206-161">Требование</span><span class="sxs-lookup"><span data-stu-id="75206-161">Requirement</span></span> | <span data-ttu-id="75206-162">Значение</span><span class="sxs-lookup"><span data-stu-id="75206-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="75206-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="75206-163">Minimum supported client</span></span><br/> | <span data-ttu-id="75206-164">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75206-164">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="75206-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="75206-165">Minimum supported server</span></span><br/> | <span data-ttu-id="75206-166">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="75206-166">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="75206-167">Header</span><span class="sxs-lookup"><span data-stu-id="75206-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="75206-168"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="75206-168"><dt>Wia.h</dt></span></span> </dl> |



 

 
