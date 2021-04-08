---
title: Свойство Дефаултвмконфигуратионпас Ивмвиртуалпк (Впккоминтерфацес. h)
description: Каталог по умолчанию для поиска доступных файлов конфигурации виртуальной машины.
ms.assetid: 9ae63198-e3f6-4dcb-8edb-85adfbbdca26
keywords:
- Дефаултвмконфигуратионпас свойство Virtual PC
- Дефаултвмконфигуратионпас свойство Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, свойство Дефаултвмконфигуратионпас
topic_type:
- apiref
api_name:
- IVMVirtualPC.DefaultVMConfigurationPath
- IVMVirtualPC.get_DefaultVMConfigurationPath
- IVMVirtualPC.put_DefaultVMConfigurationPath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e13fc2323cb15bdbeb8c42e61810a376e49b3988
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803197"
---
# <a name="ivmvirtualpcdefaultvmconfigurationpath-property"></a><span data-ttu-id="2507a-106">Ивмвиртуалпк: свойство Ефаултвмконфигуратионпас:D</span><span class="sxs-lookup"><span data-stu-id="2507a-106">IVMVirtualPC::DefaultVMConfigurationPath property</span></span>

<span data-ttu-id="2507a-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2507a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2507a-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2507a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2507a-109">Извлекает и задает каталог по умолчанию для поиска доступных файлов конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2507a-109">Retrieves and sets the default directory to be searched for available virtual machine configuration files.</span></span>

<span data-ttu-id="2507a-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="2507a-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2507a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2507a-111">Syntax</span></span>


```C++
HRESULT put_DefaultVMConfigurationPath(
  [in]          BSTR configurationPath
);

HRESULT get_DefaultVMConfigurationPath(
  [out, retval] BSTR *configurationPath
);
```



## <a name="property-value"></a><span data-ttu-id="2507a-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="2507a-112">Property value</span></span>

<span data-ttu-id="2507a-113">Указывает путь к каталогу для файлов конфигурации виртуальной машины по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2507a-113">Specifies the directory path for the default virtual machine configuration files.</span></span> <span data-ttu-id="2507a-114">В строке пути обратная косая черта ( \) может появляться непосредственно перед завершающим нулевым символом.</span><span class="sxs-lookup"><span data-stu-id="2507a-114">In the path string, a backslash (\) may appear immediately before the terminating null character.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2507a-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="2507a-115">Error codes</span></span>



| <span data-ttu-id="2507a-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="2507a-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="2507a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2507a-117">Meaning</span></span>                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2507a-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2507a-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="2507a-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2507a-119">The operation was successful.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="2507a-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="2507a-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="2507a-121">Параметр *configurationPath* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2507a-121">The *configurationPath* parameter is **NULL**.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="2507a-122"><dt>Значение HRESULT \_ ИЗ \_ Win32 ( \_ файл ошибки \_ не \_ найден)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="2507a-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="2507a-123">Системе не удается найти каталог, указанный параметром *configurationPath* .</span><span class="sxs-lookup"><span data-stu-id="2507a-123">The system cannot find the directory specified by the *configurationPath* parameter.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="2507a-124"><dt>Значение HRESULT \_ ИЗ \_ Win32 ( \_ путь ошибки \_ не \_ найден)</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="2507a-124"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="2507a-125">Системе не удается найти путь, указанный параметром *configurationPath* .</span><span class="sxs-lookup"><span data-stu-id="2507a-125">The system cannot find the path specified by the *configurationPath* parameter.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="2507a-126"><dt>Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ недопустимое \_ имя)</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="2507a-126"><dt>HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="2507a-127">Параметр *configurationPath* содержит недопустимый символ (один из следующих: " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="2507a-127">The *configurationPath* parameter contains an invalid character (one of the following: "\*?<>/\|":").</span></span><br/>                                   |
| <dl> <span data-ttu-id="2507a-128"><dt>Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ Bad \_ PATHNAME)</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="2507a-128"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="2507a-129">Параметр *configurationPath* указывает пустой или относительный путь.</span><span class="sxs-lookup"><span data-stu-id="2507a-129">The *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="2507a-130">Требуется абсолютный путь.</span><span class="sxs-lookup"><span data-stu-id="2507a-130">An absolute path is required.</span></span><br/>                                          |
| <dl> <span data-ttu-id="2507a-131"><dt>Значение HRESULT \_ ИЗ \_ Win32 ( \_ \_ переполнение буфера ошибки)</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="2507a-131"><dt>HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="2507a-132">Путь, указанный в параметре *configurationPath* , слишком длинный.</span><span class="sxs-lookup"><span data-stu-id="2507a-132">The path specified by the *configurationPath* parameter is too long.</span></span> <span data-ttu-id="2507a-133">Длина пути должна быть меньше **максимального \_ пути** (260) символов.</span><span class="sxs-lookup"><span data-stu-id="2507a-133">The length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="2507a-134"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2507a-134"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="2507a-135">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2507a-135">An unexpected error has occurred.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="2507a-136"><dt>Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="2507a-136"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="2507a-137">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="2507a-137">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                          |



## <a name="remarks"></a><span data-ttu-id="2507a-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2507a-138">Remarks</span></span>

<span data-ttu-id="2507a-139">По умолчанию для этого свойства задан следующий каталог: "% LocalAppData% виртуальных \\ \\ машин Microsoft Windows Virtual PC \\ \\ ".</span><span class="sxs-lookup"><span data-stu-id="2507a-139">By default, this property value is set to the following directory: "%LocalAppData%\\Microsoft\\Windows Virtual PC\\Virtual Machines\\".</span></span>

## <a name="requirements"></a><span data-ttu-id="2507a-140">Требования</span><span class="sxs-lookup"><span data-stu-id="2507a-140">Requirements</span></span>



| <span data-ttu-id="2507a-141">Требование</span><span class="sxs-lookup"><span data-stu-id="2507a-141">Requirement</span></span> | <span data-ttu-id="2507a-142">Значение</span><span class="sxs-lookup"><span data-stu-id="2507a-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2507a-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2507a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="2507a-144">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2507a-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2507a-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2507a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="2507a-146">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2507a-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2507a-147">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2507a-147">End of client support</span></span><br/>    | <span data-ttu-id="2507a-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2507a-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2507a-149">Продукт</span><span class="sxs-lookup"><span data-stu-id="2507a-149">Product</span></span><br/>                  | <span data-ttu-id="2507a-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2507a-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2507a-151">Header</span><span class="sxs-lookup"><span data-stu-id="2507a-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="2507a-152"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="2507a-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2507a-153">IID</span><span class="sxs-lookup"><span data-stu-id="2507a-153">IID</span></span><br/>                      | <span data-ttu-id="2507a-154">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="2507a-154">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="2507a-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2507a-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2507a-156">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="2507a-156">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

