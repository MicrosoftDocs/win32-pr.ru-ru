---
description: Устанавливает пакет исключений.
ms.assetid: c4c3c01c-9aaf-42cd-a690-13e2113b15b3
title: Функция Инсталлкомпонентв
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallComponentW
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: 4d262322be6084429f03d5725f61c0e0f7140871
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657709"
---
# <a name="installcomponentw-function"></a><span data-ttu-id="7bdca-103">Функция Инсталлкомпонентв</span><span class="sxs-lookup"><span data-stu-id="7bdca-103">InstallComponentW function</span></span>

<span data-ttu-id="7bdca-104">Устанавливает пакет исключений.</span><span class="sxs-lookup"><span data-stu-id="7bdca-104">Installs an exception package.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bdca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7bdca-105">Syntax</span></span>


```C++
void InstallComponentW(
  _In_           LPCWSTR InfPath,
  _In_opt_ const GUID    *CompGuid,
  _In_           DWORD   Flags,
  _In_opt_       INT     VerMajor,
  _In_opt_       INT     VerMinor,
  _In_opt_       INT     VerBuild,
  _In_opt_       INT     VerQFE,
  _In_opt_       LPCWSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="7bdca-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7bdca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bdca-107">*Инфпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7bdca-107">*InfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bdca-108">Путь к INF-файлу исключения для обработки.</span><span class="sxs-lookup"><span data-stu-id="7bdca-108">The path to the exception INF to process.</span></span>

</dd> <dt>

<span data-ttu-id="7bdca-109">*Компгуид* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="7bdca-109">*CompGuid* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7bdca-110">Идентификатор GUID устанавливаемого компонента исключения.</span><span class="sxs-lookup"><span data-stu-id="7bdca-110">The GUID of the exception component being installed.</span></span>

</dd> <dt>

<span data-ttu-id="7bdca-111">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7bdca-111">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bdca-112">Флаги, используемые для управления поведением при установке.</span><span class="sxs-lookup"><span data-stu-id="7bdca-112">The flags used to control installation behaviors.</span></span> <span data-ttu-id="7bdca-113">Этот параметр может быть сочетанием следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7bdca-113">This parameter can be a combination of the following values.</span></span>



| <span data-ttu-id="7bdca-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7bdca-114">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="7bdca-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7bdca-115">Meaning</span></span>                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_FORCE"></span><span id="comp_flags_force"></span><dl> <span data-ttu-id="7bdca-116"><dt>**Comp \_ FLAGs \_ Force**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="7bdca-116"><dt>**COMP\_FLAGS\_FORCE**</dt> <dt>0x00000020</dt></span></span> </dl>                             | <span data-ttu-id="7bdca-117">Пропускает проверку версий для замен файлов.</span><span class="sxs-lookup"><span data-stu-id="7bdca-117">Skips the version check on file replacements.</span></span><br/>                                                                                                    |
| <span id="COMP_FLAGS_NEEDS_UNINSTALL"></span><span id="comp_flags_needs_uninstall"></span><dl> <span data-ttu-id="7bdca-118"><dt>**Comp \_ \_требуется \_ Удаление флагов**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="7bdca-118"><dt>**COMP\_FLAGS\_NEEDS\_UNINSTALL**</dt> <dt></dt></span></span> </dl>        | <span data-ttu-id="7bdca-119">Резервное копирование файлов, которые обновляются для использования при удалении компонента.</span><span class="sxs-lookup"><span data-stu-id="7bdca-119">Back up files that are updated to be used by an uninstall of the component.</span></span><br/>                                                                      |
| <span id="COMP_FLAGS_NO_OVERWRITE"></span><span id="comp_flags_no_overwrite"></span><dl> <span data-ttu-id="7bdca-120"><dt>**Comp \_ ФЛАГи \_ без \_ перезаписи**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="7bdca-120"><dt>**COMP\_FLAGS\_NO\_OVERWRITE**</dt> <dt></dt></span></span> </dl>                 | <span data-ttu-id="7bdca-121">Пропускает резервное копирование файлов, если версия компонента исключения совпадает с установленным компонентом.</span><span class="sxs-lookup"><span data-stu-id="7bdca-121">Skips backing up files if the Exception component version is the same as an installed component.</span></span> <span data-ttu-id="7bdca-122">Этот флаг используется в сценарии переустановки.</span><span class="sxs-lookup"><span data-stu-id="7bdca-122">This flag is used in a reinstallation scenario.</span></span><br/> |
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <span data-ttu-id="7bdca-123"><dt>**Comp \_ ФЛАГи \_ NOUI)**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="7bdca-123"><dt>**COMP\_FLAGS\_NOUI**</dt> <dt>0x00000002</dt></span></span> </dl>                                | <span data-ttu-id="7bdca-124">Подавляет весь пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="7bdca-124">Suppresses all UI.</span></span><br/>                                                                                                                               |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <span data-ttu-id="7bdca-125"><dt>**Comp \_ ФЛАГ \_ обновления \_ DLLCACHE**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="7bdca-125"><dt>**COMP\_FLAGS\_UPDATE\_DLLCACHE**</dt> <dt></dt></span></span> </dl>        | <span data-ttu-id="7bdca-126">Принудительное обновление каталога DLLCACHE при обновлении системного файла.</span><span class="sxs-lookup"><span data-stu-id="7bdca-126">Forces the DLLCACHE directory to be updated when a system file is updated.</span></span><br/>                                                                       |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <span data-ttu-id="7bdca-127"><dt>**Comp \_ ФЛАГи \_ используют \_ \_ кэш SVCPACK**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="7bdca-127"><dt>**COMP\_FLAGS\_USE\_SVCPACK\_CACHE**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="7bdca-128">Использует файлы, кэшированные при установке пакета обновления Windows, для замены резервных копий файлов.</span><span class="sxs-lookup"><span data-stu-id="7bdca-128">Uses files cached by a Windows service pack install to supersede files backed up.</span></span><br/>                                                                |



 

</dd> <dt>

<span data-ttu-id="7bdca-129">*Вермажор* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="7bdca-129">*VerMajor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7bdca-130">Основной номер версии компонента исключения.</span><span class="sxs-lookup"><span data-stu-id="7bdca-130">The major version of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="7bdca-131">*Верминор* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="7bdca-131">*VerMinor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7bdca-132">Дополнительный номер версии компонента исключения.</span><span class="sxs-lookup"><span data-stu-id="7bdca-132">The minor version of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="7bdca-133">*Вербуилд* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="7bdca-133">*VerBuild* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7bdca-134">Версия сборки компонента исключения.</span><span class="sxs-lookup"><span data-stu-id="7bdca-134">The build version of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="7bdca-135">*Веркфе* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="7bdca-135">*VerQFE* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7bdca-136">Редакция исправления компонента исключения.</span><span class="sxs-lookup"><span data-stu-id="7bdca-136">The hotfix revision of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="7bdca-137">*Имя* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="7bdca-137">*Name* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7bdca-138">Описательная строка компонента, отображаемая в диалоговом окне Защита файлов Windows, если операционная система обнаруживает, что файл защиты файлов Windows поврежден, незаконно изменен или поврежден.</span><span class="sxs-lookup"><span data-stu-id="7bdca-138">The descriptive string of the component shown by the Windows File Protection dialog box if the operating system detects that a Windows File Protection protect file is damaged, tampered with, or corrupted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bdca-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7bdca-139">Return value</span></span>

<span data-ttu-id="7bdca-140">Эта функция возвращает значение **HRESULT** (S \_ OK или код ошибки).</span><span class="sxs-lookup"><span data-stu-id="7bdca-140">This function returns an **HRESULT** value (S\_OK or a failure code).</span></span> <span data-ttu-id="7bdca-141">Код ошибки можно проверить на соответствие значению 0x20000100, чтобы определить, является ли сбой необходимым, поскольку требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="7bdca-141">A failure code can be checked against a value of 0x20000100 to determine whether the failure is because a reboot is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bdca-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7bdca-142">Remarks</span></span>

<span data-ttu-id="7bdca-143">Пакеты исключений — это системные файлы Windows, выпущенные за пределами полной версии пакета Windows и обновленными файлами операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7bdca-143">Exception packages are Windows system files that are released outside of a full package Windows release and that update operating-system files.</span></span> <span data-ttu-id="7bdca-144">Пакеты исключений разрабатываются только командами операционной системы, которым была предоставлена авторизация на обновление системных файлов Windows.</span><span class="sxs-lookup"><span data-stu-id="7bdca-144">Exception packages are authored only by operating-system teams that have been granted authorization to update Windows system files.</span></span>

<span data-ttu-id="7bdca-145">Для установки и удаления файлов, не защищенных с помощью защиты файлов Windows, используйте функции, описанные в статье [Общие функции установки](https://msdn.microsoft.com/library/ms794585.aspx).</span><span class="sxs-lookup"><span data-stu-id="7bdca-145">To install and uninstall files that are not protected by Windows File Protection, use the functions documented in [General Setup Functions](https://msdn.microsoft.com/library/ms794585.aspx).</span></span> <span data-ttu-id="7bdca-146">Чтобы установить драйверы устройств, поставщиков следует использовать функции, описанные в статье [функции установки устройств](https://msdn.microsoft.com/library/ms792954.aspx) и [функции PnP Configuration Manager](https://msdn.microsoft.com/library/ms790838.aspx).</span><span class="sxs-lookup"><span data-stu-id="7bdca-146">To install device drivers, venders should use functions documented in [Device Installation Functions](https://msdn.microsoft.com/library/ms792954.aspx) and [PnP Configuration Manager Functions](https://msdn.microsoft.com/library/ms790838.aspx).</span></span>

<span data-ttu-id="7bdca-147">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="7bdca-147">This function has no associated import library or header file; you must call it by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bdca-148">Требования</span><span class="sxs-lookup"><span data-stu-id="7bdca-148">Requirements</span></span>



| <span data-ttu-id="7bdca-149">Требование</span><span class="sxs-lookup"><span data-stu-id="7bdca-149">Requirement</span></span> | <span data-ttu-id="7bdca-150">Значение</span><span class="sxs-lookup"><span data-stu-id="7bdca-150">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bdca-151">DLL</span><span class="sxs-lookup"><span data-stu-id="7bdca-151">DLL</span></span><br/> | <dl> <span data-ttu-id="7bdca-152"><dt>Msoobci.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bdca-152"><dt>Msoobci.dll</dt></span></span> </dl> |



 

 
