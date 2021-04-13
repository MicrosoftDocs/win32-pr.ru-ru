---
description: Удаляет пакет исключения.
ms.assetid: d590d0f8-c9b2-4973-999b-99bbf94d4928
title: Функция Унинсталлкомпонент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UninstallComponent
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: a541f51b030c9be7a26d573794e4df3a7cfc6f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647934"
---
# <a name="uninstallcomponent-function"></a><span data-ttu-id="f5c4c-103">Функция Унинсталлкомпонент</span><span class="sxs-lookup"><span data-stu-id="f5c4c-103">UninstallComponent function</span></span>

<span data-ttu-id="f5c4c-104">Удаляет пакет исключения.</span><span class="sxs-lookup"><span data-stu-id="f5c4c-104">Removes an exception package.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5c4c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5c4c-105">Syntax</span></span>


```C++
void UninstallComponent(
  _In_opt_ const GUID  *CompGuid,
  _In_           DWORD Flags,
  _In_opt_       INT   VerMajor,
  _In_opt_       INT   VerMinor,
  _In_opt_       INT   VerBuild,
  _In_opt_       INT   VerQFE
);
```



## <a name="parameters"></a><span data-ttu-id="f5c4c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5c4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5c4c-107">*Компгуид* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f5c4c-107">*CompGuid* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f5c4c-108">Идентификатор GUID удаляемого компонента исключения.</span><span class="sxs-lookup"><span data-stu-id="f5c4c-108">The GUID of the exception component being uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="f5c4c-109">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f5c4c-109">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5c4c-110">Флаги, используемые для управления поведением при установке.</span><span class="sxs-lookup"><span data-stu-id="f5c4c-110">The flags used to control installation behaviors.</span></span> <span data-ttu-id="f5c4c-111">Этот параметр может быть сочетанием следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f5c4c-111">This parameter can be a combination of the following values.</span></span>



| <span data-ttu-id="f5c4c-112">Значение</span><span class="sxs-lookup"><span data-stu-id="f5c4c-112">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="f5c4c-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f5c4c-113">Meaning</span></span>                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <span data-ttu-id="f5c4c-114"><dt>**\_NOUI) флаги Comp \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f5c4c-114"><dt>**COMP\_FLAGS\_NOUI**</dt></span></span> </dl>                                          | <span data-ttu-id="f5c4c-115">Подавляет весь пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="f5c4c-115">Suppresses all UI.</span></span><br/>                                                                |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <span data-ttu-id="f5c4c-116"><dt>**\_Флаги Comp \_ обновления \_ DLLCACHE**</dt></span><span class="sxs-lookup"><span data-stu-id="f5c4c-116"><dt>**COMP\_FLAGS\_UPDATE\_DLLCACHE**</dt></span></span> </dl>        | <span data-ttu-id="f5c4c-117">Принудительное обновление каталога DLLCACHE при обновлении системного файла.</span><span class="sxs-lookup"><span data-stu-id="f5c4c-117">Forces the DLLCACHE directory to be updated when a system file is updated.</span></span><br/>        |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <span data-ttu-id="f5c4c-118"><dt>**\_Флаги \_ comp \_ используют \_ кэш SVCPACK**</dt></span><span class="sxs-lookup"><span data-stu-id="f5c4c-118"><dt>**COMP\_FLAGS\_USE\_SVCPACK\_CACHE**</dt></span></span> </dl> | <span data-ttu-id="f5c4c-119">Использует файлы, кэшированные при установке пакета обновления Windows, для замены резервных копий файлов.</span><span class="sxs-lookup"><span data-stu-id="f5c4c-119">Uses files cached by a Windows service pack install to supersede files backed up.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f5c4c-120">*Вермажор* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f5c4c-120">*VerMajor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f5c4c-121">Основная версия компонента исключения, который необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="f5c4c-121">The major version of the Exception component to be uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="f5c4c-122">*Верминор* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f5c4c-122">*VerMinor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f5c4c-123">Дополнительный номер версии компонента исключения, который необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="f5c4c-123">The minor version of the Exception component to be uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="f5c4c-124">*Вербуилд* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f5c4c-124">*VerBuild* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f5c4c-125">Версия сборки компонента исключения, который необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="f5c4c-125">The build version of the Exception component to be uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="f5c4c-126">*Веркфе* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f5c4c-126">*VerQFE* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f5c4c-127">Редакция исправления компонента исключения, который необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="f5c4c-127">The hotfix revision of the Exception component to be uninstalled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5c4c-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5c4c-128">Return value</span></span>

<span data-ttu-id="f5c4c-129">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f5c4c-129">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5c4c-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5c4c-130">Remarks</span></span>

<span data-ttu-id="f5c4c-131">Пакеты исключений — это системные файлы Windows, выпущенные за пределами полной версии пакета Windows и обновленными файлами операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f5c4c-131">Exception packages are Windows system files that are released outside of a full package Windows release and that update operating-system files.</span></span> <span data-ttu-id="f5c4c-132">Пакеты исключений разрабатываются только командами операционной системы, которым была предоставлена авторизация на обновление системных файлов Windows.</span><span class="sxs-lookup"><span data-stu-id="f5c4c-132">Exception packages are authored only by operating-system teams that have been granted authorization to update Windows system files.</span></span>

<span data-ttu-id="f5c4c-133">Для установки и удаления файлов, не защищенных с помощью защиты файлов Windows, используйте функции, описанные в статье [Общие функции установки](https://msdn.microsoft.com/library/ms794585.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5c4c-133">To install and uninstall files that are not protected by Windows File Protection, use the functions documented in [General Setup Functions](https://msdn.microsoft.com/library/ms794585.aspx).</span></span> <span data-ttu-id="f5c4c-134">Чтобы установить драйверы устройств, поставщиков следует использовать функции, описанные в статье [функции установки устройств](https://msdn.microsoft.com/library/ms792954.aspx) и [функции PnP Configuration Manager](https://msdn.microsoft.com/library/ms790838.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5c4c-134">To install device drivers, venders should use functions documented in [Device Installation Functions](https://msdn.microsoft.com/library/ms792954.aspx) and [PnP Configuration Manager Functions](https://msdn.microsoft.com/library/ms790838.aspx).</span></span>

<span data-ttu-id="f5c4c-135">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="f5c4c-135">This function has no associated import library or header file; you must call it by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5c4c-136">Требования</span><span class="sxs-lookup"><span data-stu-id="f5c4c-136">Requirements</span></span>



| <span data-ttu-id="f5c4c-137">Требование</span><span class="sxs-lookup"><span data-stu-id="f5c4c-137">Requirement</span></span> | <span data-ttu-id="f5c4c-138">Значение</span><span class="sxs-lookup"><span data-stu-id="f5c4c-138">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c4c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f5c4c-139">DLL</span></span><br/> | <dl> <span data-ttu-id="f5c4c-140"><dt>Msoobci.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5c4c-140"><dt>Msoobci.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5c4c-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5c4c-141">See also</span></span>

<dl> <span data-ttu-id="f5c4c-142"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="f5c4c-142"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="f5c4c-143">**инсталлкомпонентв**</span><span class="sxs-lookup"><span data-stu-id="f5c4c-143">**InstallComponentW**</span></span>](installcomponentw.md)
</dt> </dl>

 

 
