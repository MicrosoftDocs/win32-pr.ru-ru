---
description: Метод Провидекуалифиедкомпонент объекта Installer возвращает полный путь к компоненту и выполняет все необходимые установки. При необходимости этот метод запрашивает источник и увеличивает счетчик использования для функции.
ms.assetid: 4f9a5094-1556-4d86-8b51-c8c3ce1cbed4
title: Метод Installer. Провидекуалифиедкомпонент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideQualifiedComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 73c830610b49976e3625dd333c57f39e43d4be14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651983"
---
# <a name="installerprovidequalifiedcomponent-method"></a><span data-ttu-id="e1381-104">Метод Installer. Провидекуалифиедкомпонент</span><span class="sxs-lookup"><span data-stu-id="e1381-104">Installer.ProvideQualifiedComponent method</span></span>

<span data-ttu-id="e1381-105">Метод **провидекуалифиедкомпонент** объекта [**Installer**](installer-object.md) возвращает полный путь к компоненту и выполняет все необходимые установки.</span><span class="sxs-lookup"><span data-stu-id="e1381-105">The **ProvideQualifiedComponent** method of the [**Installer**](installer-object.md) object returns the full component path and performs any necessary installation.</span></span> <span data-ttu-id="e1381-106">При необходимости этот метод запрашивает источник и увеличивает счетчик использования для функции.</span><span class="sxs-lookup"><span data-stu-id="e1381-106">If necessary, this method prompts for the source and increments the usage count for the feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1381-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1381-107">Syntax</span></span>


```JScript
Installer.ProvideQualifiedComponent(
  Category,
  Qualifier,
  InstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="e1381-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1381-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1381-109">*Категория*</span><span class="sxs-lookup"><span data-stu-id="e1381-109">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="e1381-110">Указывает идентификатор компонента для запрошенного компонента.</span><span class="sxs-lookup"><span data-stu-id="e1381-110">Specifies the component ID for the requested component.</span></span> <span data-ttu-id="e1381-111">Это может быть не GUID самого компонента, а сервера, который предоставляет правильные функциональные возможности, как в столбце ComponentId [таблицы публишкомпонент](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="e1381-111">This may not be the GUID for the component itself but rather a server that provides the correct functionality, as in the ComponentId column of the [PublishComponent table](publishcomponent-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1381-112">*Квалификатор*</span><span class="sxs-lookup"><span data-stu-id="e1381-112">*Qualifier*</span></span> 
</dt> <dd>

<span data-ttu-id="e1381-113">Указывает квалификатор в списке компонентов рекламы (из [таблицы публишкомпонент](publishcomponent-table.md)).</span><span class="sxs-lookup"><span data-stu-id="e1381-113">Specifies a qualifier into a list of advertising components (from [PublishComponent table](publishcomponent-table.md)).</span></span>

</dd> <dt>

<span data-ttu-id="e1381-114">*InstallMode*</span><span class="sxs-lookup"><span data-stu-id="e1381-114">*InstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="e1381-115">Определяет режим установки.</span><span class="sxs-lookup"><span data-stu-id="e1381-115">Defines the installation mode.</span></span> <span data-ttu-id="e1381-116">Этот параметр может принимать одно из значений, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e1381-116">This parameter can be one of the values shown in the following table.</span></span>



| <span data-ttu-id="e1381-117">InstallMode</span><span class="sxs-lookup"><span data-stu-id="e1381-117">InstallMode</span></span>                                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="e1381-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e1381-118">Meaning</span></span>                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <span data-ttu-id="e1381-119"><dt>**мсиинсталлмодедефаулт**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e1381-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span></span> </dl>                                                                                 | <span data-ttu-id="e1381-120">Предоставляет компонент, выполняющий необходимую установку.</span><span class="sxs-lookup"><span data-stu-id="e1381-120">Provides the component, performing any necessary installation.</span></span><br/>                                                                                                                                                           |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <span data-ttu-id="e1381-121"><dt>**мсиинсталлмодиксистинг**</dt> <dt>— 1</dt></span><span class="sxs-lookup"><span data-stu-id="e1381-121"><dt>**msiInstallModeExisting**</dt> <dt>–1</dt></span></span> </dl>                                                                            | <span data-ttu-id="e1381-122">Предоставляет компонент только в том случае, если компонент существует. в противном случае возвращает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="e1381-122">Provides the component only if the feature exists; otherwise returns an empty string.</span></span> <span data-ttu-id="e1381-123">Этот режим проверяет существование файла ключа компонента.</span><span class="sxs-lookup"><span data-stu-id="e1381-123">This mode verifies the existence of the component's key file.</span></span><br/>                                                                      |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <span data-ttu-id="e1381-124"><dt>**мсиинсталлмоденодетектион**</dt> <dt>– 2</dt></span><span class="sxs-lookup"><span data-stu-id="e1381-124"><dt>**msiInstallModeNoDetection**</dt> <dt>–2</dt></span></span> </dl>                                                                | <span data-ttu-id="e1381-125">Предоставляет компонент только в том случае, если компонент существует. в противном случае возвращает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="e1381-125">Provides the component only if the feature exists; otherwise returns an empty string.</span></span> <span data-ttu-id="e1381-126">Этот режим проверяет, что компонент зарегистрирован, но не проверяет существование файла ключа компонента.</span><span class="sxs-lookup"><span data-stu-id="e1381-126">This mode only checks that the component is registered but does not verify the existence of the component's key file.</span></span><br/>              |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <span data-ttu-id="e1381-127"><dt>**мсиинсталлмоденосаурцересолутион**</dt> <dt>– 3</dt></span><span class="sxs-lookup"><span data-stu-id="e1381-127"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>–3</dt></span></span> </dl>                                    | <span data-ttu-id="e1381-128">Предоставляет путь к компоненту только в том случае, если компонент существует с параметром InstallState параметра *мсиинсталлстателокал*.</span><span class="sxs-lookup"><span data-stu-id="e1381-128">Provides the component path only if the feature exists with an InstallState parameter of *msiInstallStateLocal*.</span></span> <span data-ttu-id="e1381-129">При этом проверяется регистрация компонента, но не проверяется наличие файла ключа компонента.</span><span class="sxs-lookup"><span data-stu-id="e1381-129">This checks the component's registration but does not verify the existence of the component's key file.</span></span><br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <span data-ttu-id="e1381-130"><dt>**сочетание флагов мсиреинсталлмоде**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e1381-130"><dt>**combination of the msiReinstallMode flags**</dt> <dt> </dt></span></span> </dl> | <span data-ttu-id="e1381-131">Вызывает [**реинсталлфеатуре**](installer-reinstallfeature.md) для переустановки компонента с помощью этого параметра для параметра *ReinstallMode* , а затем предоставляет компонент.</span><span class="sxs-lookup"><span data-stu-id="e1381-131">Calls [**ReinstallFeature**](installer-reinstallfeature.md) to reinstall the feature using this parameter for the *ReinstallMode* parameter, and then provides the component.</span></span><br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1381-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1381-132">Return value</span></span>

<span data-ttu-id="e1381-133">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e1381-133">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1381-134">Требования</span><span class="sxs-lookup"><span data-stu-id="e1381-134">Requirements</span></span>



| <span data-ttu-id="e1381-135">Требование</span><span class="sxs-lookup"><span data-stu-id="e1381-135">Requirement</span></span> | <span data-ttu-id="e1381-136">Значение</span><span class="sxs-lookup"><span data-stu-id="e1381-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1381-137">Версия</span><span class="sxs-lookup"><span data-stu-id="e1381-137">Version</span></span><br/> | <span data-ttu-id="e1381-138">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e1381-138">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e1381-139">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e1381-139">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e1381-140">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="e1381-140">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e1381-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e1381-141">DLL</span></span><br/>     | <dl> <span data-ttu-id="e1381-142"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1381-142"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e1381-143">IID</span><span class="sxs-lookup"><span data-stu-id="e1381-143">IID</span></span><br/>     | <span data-ttu-id="e1381-144">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e1381-144">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="e1381-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1381-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1381-146">**мсипровидекуалифиедкомпонент**</span><span class="sxs-lookup"><span data-stu-id="e1381-146">**MsiProvideQualifiedComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
</dt> </dl>

 

 




