---
description: Создает объект Save. Не рекомендуется.
ms.assetid: 50a7dbde-1dd4-4aae-a9ab-97d6f99618c0
title: 'Метод Идиректксфиле:: Креатесавеобжект (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 848010a1f701b39f5cc77a126272bc019ed01f4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664995"
---
# <a name="idirectxfilecreatesaveobject-method"></a><span data-ttu-id="3b097-104">Метод Идиректксфиле:: Креатесавеобжект</span><span class="sxs-lookup"><span data-stu-id="3b097-104">IDirectXFile::CreateSaveObject method</span></span>

<span data-ttu-id="3b097-105">Создает объект Save.</span><span class="sxs-lookup"><span data-stu-id="3b097-105">Creates a save object.</span></span> <span data-ttu-id="3b097-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="3b097-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b097-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b097-107">Syntax</span></span>


```C++
HRESULT CreateSaveObject(
  [in]          LPCSTR                  szFileName,
  [in]          DXFILEFORMAT            dwFileFormat,
  [out, retval] LPDIRECTXFILESAVEOBJECT *ppSaveObj
);
```



## <a name="parameters"></a><span data-ttu-id="3b097-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b097-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b097-109">*сзфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3b097-109">*szFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b097-110">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3b097-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3b097-111">Указатель на имя файла, используемого для сохранения данных.</span><span class="sxs-lookup"><span data-stu-id="3b097-111">Pointer to the name of the file to use for saving data.</span></span>

</dd> <dt>

<span data-ttu-id="3b097-112">*двфилеформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3b097-112">*dwFileFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b097-113">Тип: **[ **дксфилеформат**](dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="3b097-113">Type: **[**DXFILEFORMAT**](dxfile.md)**</span></span>

<span data-ttu-id="3b097-114">Указывает формат, используемый при сохранении файла DirectX.</span><span class="sxs-lookup"><span data-stu-id="3b097-114">Indicates the format to use when saving the DirectX file.</span></span> <span data-ttu-id="3b097-115">Это значение может быть одним из \_ флагов дксфилеформат XXX в [константах дксфиле](dxfile.md).</span><span class="sxs-lookup"><span data-stu-id="3b097-115">This value can be one of the DXFILEFORMAT\_xxx flags in [DXFILE Constants](dxfile.md).</span></span> <span data-ttu-id="3b097-116">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="3b097-116">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3b097-117">*ппсавеобж* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3b097-117">*ppSaveObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3b097-118">Тип: **[ **лпдиректксфилесавеобжект**](idirectxfilesaveobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="3b097-118">Type: **[**LPDIRECTXFILESAVEOBJECT**](idirectxfilesaveobject.md)\***</span></span>

<span data-ttu-id="3b097-119">Адрес указателя на интерфейс [**идиректксфилесавеобжект**](idirectxfilesaveobject.md) , представляющий созданный объект Save.</span><span class="sxs-lookup"><span data-stu-id="3b097-119">Address of a pointer to an [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) interface, representing the created save object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b097-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b097-120">Return value</span></span>

<span data-ttu-id="3b097-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3b097-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3b097-122">Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3b097-122">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="3b097-123">В случае сбоя метода возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадаллок, дксфилирр \_ БАДФИЛЕ, дксфилирр \_ бадвалуе.</span><span class="sxs-lookup"><span data-stu-id="3b097-123">If the method fails, the return value can be one of the following: DXFILEERR\_BADALLOC, DXFILEERR\_BADFILE, DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b097-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b097-124">Remarks</span></span>

<span data-ttu-id="3b097-125">После использования этого метода используйте методы интерфейса [**идиректксфилесавеобжект**](idirectxfilesaveobject.md) для создания объектов данных и сохранения шаблонов или данных.</span><span class="sxs-lookup"><span data-stu-id="3b097-125">After using this method, use methods of the [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) interface to create data objects and to save templates or data.</span></span>

<span data-ttu-id="3b097-126">Значение по умолчанию для формата файла — ДКСФИЛЕФОРМАТ \_ binary.</span><span class="sxs-lookup"><span data-stu-id="3b097-126">The default value for the file format is DXFILEFORMAT\_BINARY.</span></span> <span data-ttu-id="3b097-127">Значения формата файла можно комбинировать в логическом или для создания сжатого текста или сжатых двоичных файлов.</span><span class="sxs-lookup"><span data-stu-id="3b097-127">The file format values can be combined in a logical OR to create compressed text or compressed binary files.</span></span> <span data-ttu-id="3b097-128">Если файл указан как двоичный (0) и Text (1), то он будет сохранен как текстовый файл, поскольку значение будет неразличимым из значения формата текстового файла (0 + 1 = 1).</span><span class="sxs-lookup"><span data-stu-id="3b097-128">If a file is specified as both binary (0) and text (1), it will be saved as a text file because the value will be indistinguishable from the text file format value (0 + 1 = 1).</span></span> <span data-ttu-id="3b097-129">Если указать, что формат файла должен быть текстовым и сжатым, файл сначала будет записан как текст, а затем сжат.</span><span class="sxs-lookup"><span data-stu-id="3b097-129">If you indicate that the file format should be text and compressed, the file will first be written out as text and then compressed.</span></span> <span data-ttu-id="3b097-130">Однако сжатые текстовые файлы не настолько эффективны, как двоичные текстовые файлы, поэтому в большинстве случаев потребуется указать двоичные и сжатые данные.</span><span class="sxs-lookup"><span data-stu-id="3b097-130">However, compressed text files are not as efficient as binary text files, so in most cases you will want to indicate binary and compressed.</span></span> <span data-ttu-id="3b097-131">При настройке файла для сжатия без указания формата будет получен двоичный сжатый файл.</span><span class="sxs-lookup"><span data-stu-id="3b097-131">Setting a file to be compressed without specifying a format will result in a binary, compressed file.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b097-132">Требования</span><span class="sxs-lookup"><span data-stu-id="3b097-132">Requirements</span></span>



| <span data-ttu-id="3b097-133">Требование</span><span class="sxs-lookup"><span data-stu-id="3b097-133">Requirement</span></span> | <span data-ttu-id="3b097-134">Значение</span><span class="sxs-lookup"><span data-stu-id="3b097-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b097-135">Header</span><span class="sxs-lookup"><span data-stu-id="3b097-135">Header</span></span><br/>  | <dl> <span data-ttu-id="3b097-136"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b097-136"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b097-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3b097-137">Library</span></span><br/> | <dl> <span data-ttu-id="3b097-138"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b097-138"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b097-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b097-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b097-140">идиректксфиле</span><span class="sxs-lookup"><span data-stu-id="3b097-140">IDirectXFile</span></span>](idirectxfile.md)
</dt> <dt>

[<span data-ttu-id="3b097-141">**идиректксфилесавеобжект**</span><span class="sxs-lookup"><span data-stu-id="3b097-141">**IDirectXFileSaveObject**</span></span>](idirectxfilesaveobject.md)
</dt> </dl>

 

 
