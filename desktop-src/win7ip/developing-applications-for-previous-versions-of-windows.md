---
title: Разработка приложений для предыдущих версий Windows
description: объясняет, что нужно сделать для разработки приложений, выполняемых в предыдущих версиях Windows и воспользоваться преимуществами API, которые поддерживаются в обновлении платформы для Windows Vista и обновления платформы для Windows Server 2008.
ms.assetid: 9c46f894-e5cd-46a1-81c8-f63b09504735
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afbb999faf934ae621f80a824eca0289ff3df705ed11d7cfd161935c944947f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549484"
---
# <a name="developing-applications-for-previous-versions-of-windows"></a>Разработка приложений для предыдущих версий Windows

объясняет, что нужно сделать для разработки приложений, выполняемых в предыдущих версиях Windows и воспользоваться преимуществами API, которые поддерживаются в обновлении платформы для Windows Vista и обновления платформы для Windows Server 2008.

## <a name="required-downloads"></a>Необходимые загрузки

загрузка и установка пакетов, описанных в следующих разделах, требуется для разработки приложений, использующих API, которые представлены в пакете Microsoft Windows Software Development Kit (SDK) для Windows 7.

### <a name="microsoft-windows-sdk"></a>Microsoft Windows SDK

Windows SDK для Windows 7 требуется для создания приложений, использующих интерфейсы api, поддерживаемые с обновлением платформы для Windows Vista и обновлением платформы для Windows Server 2008.

дополнительные ресурсы и сведения, такие как файлы для загрузки, сообщения на форуме и блог группы Windows SDK, см. в [центре разработчиков Windows SDK](https://msdn.microsoft.com/bb980924.aspx) ( https://msdn.microsoft.com/bb980924.aspx) .

### <a name="net-framework"></a>.NET Framework

пакет обновления 1 (sp1) для платформа .NET Framework 3,5 необходим для создания приложений, использующих api, которые поддерживаются обновлением платформы для Windows Vista и обновлением платформы для Windows Server 2008.

дополнительные ресурсы и сведения см. в [центре платформа .NET Framework Developer Center](https://msdn.microsoft.com/netframework/default.aspx) ( https://msdn.microsoft.com/netframework/default.aspx) .

### <a name="directx-sdk-required-when-using-direct3d"></a>При использовании Direct3D требуется пакет SDK для DirectX

при создании приложений, использующих Direct3D, [пакет SDK для DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) необходим для создания приложений, использующих api-интерфейсы, поддерживаемые обновлением платформы для Windows Vista и обновлением платформы для Windows Server 2008.

### <a name="update-your-development-computer"></a>Обновление компьютера разработчика

убедитесь, что на компьютере разработчика установлены все последние обновления от Центр обновления Windows.

при разработке приложений на более ранней версии Windows необходимо получить обновление платформы для Windows Vista или обновление платформы для Windows Server 2008 с Центр обновления Windows. установка любого из этих обновлений позволит вам воспользоваться преимуществами нового API, предоставляемого Windows SDK для Windows 7.

дополнительные сведения о получении обновлений из Центр обновления Windows см. в статье базы [знаний об обновлении платформы для Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) ( https://support.microsoft.com/kb/971644) .

## <a name="development-environment"></a>Среда разработки

### <a name="set-the-build-target-to-windows-7"></a>задайте для целевого объекта сборки значение Windows 7.

все приложения, использующие библиотеки в обновлении платформы для Windows Vista, должны быть построены на целевой платформе Windows 7.

установка параметра WINVER в значение целевой платформы Windows 7 позволяет разрабатывать приложения, использующие api, поддерживаемые с обновлением платформы для Windows Vista или обновлением платформы для Windows Server 2008 на компьютере разработки, на котором работает Windows vista.

целевую платформу можно задать для Windows 7 либо в исходном коде, либо с помощью параметра/d в компиляторе Visual Studio.

В следующем примере показано, как задать WINVER в исходном коде.


```C++
#define WINVER 0x0601
```



В следующем примере показано, как задать WINVER с помощью параметра компилятора/D.

``` syntax
/DWINVER=0x0601
```

## <a name="application-deployment"></a>Развертывание приложения

если вы создаете приложение с помощью заголовков и библиотек, предоставленных Windows SDK для Windows 7, поддерживаемые api-интерфейсы будут выполняться в любой Windows версии, где установлено обновление платформы для Windows Vista или обновление платформы для Windows Server 2008.

> [!Note]  
> поведение, производительность или требования для некоторых интерфейсов api, которые поддерживаются при обновлении платформы для Windows Vista или обновления платформы для Windows Server 2008, могут различаться в разных версиях Windows. дополнительные сведения о конкретном API, поддерживаемом обновлениями, см. в [статье об обновлении платформы для Windows Vista](platform-update-for-windows-vista-overview.md).

 

### <a name="no-redistributable-components"></a>Нет распространяемых компонентов

Приложению не требуется устанавливать распространяемые компоненты, такие как библиотеки DLL или другие файлы времени выполнения.

### <a name="requires-updated-end-user-computer"></a>Требуется обновленный End-User компьютер

поскольку обновление платформы для Windows Vista и обновление платформы для Windows Server 2008 размещаются на Центр обновления Windows, конечные пользователи с включенным автоматическим обновлением, скорее всего, уже имеют эти обновления, а также необходимые пакеты обновления.

если на компьютере конечного пользователя отсутствует обновление платформы для Windows Vista или обновление платформы для Windows Server 2008 и для приложения требуются интерфейсы api, которые поддерживаются этими обновлениями, приложение может не быть запущено на компьютере конечного пользователя или во время выполнения могут возникать ошибки.

чтобы избежать проблем, которые могут быть вызваны неактуальностью компьютера пользователя, необходимо убедиться, что на компьютере пользователя имеется обновление платформы для Windows Vista или обновление платформы для Windows Server 2008 во время установки приложения. вы можете использовать [API Центр обновления Windows агента](/windows/desktop/Wua_Sdk/portal-client) , чтобы проверить компьютер конечного пользователя на наличие установленных обновлений. вы также можете использовать API агента Центр обновления Windows, чтобы скачать и установить необходимые обновления во время установки приложения, если пользователь еще не установил обновления.

пример установщика, демонстрирующий использование [API агента Центр обновления Windows](/windows/desktop/Wua_Sdk/portal-client), см. в разделе [развертывание Direct3D 11 для разработчиков игр](../direct3darticles/direct3d11-deployment.md) в [пакете SDK DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) .

несмотря на то, что пример установщика D3D11InstallHelper, обсуждаемый в [развертывании direct3d 11 для разработчиков игр](../direct3darticles/direct3d11-deployment.md), был написан для приложений, использующих Direct3D 11, он предоставляет хороший пример взаимодействия с [API агента Центр обновления Windows](/windows/desktop/Wua_Sdk/portal-client) для инициирования и контроля загрузки и установки обновлений, размещенных в Центр обновления Windows. для компиляции этого примера может потребоваться Windows SDK для Windows 7. дополнительные сведения о примере D3D11InstallHelper, включая известные проблемы, см. в [пакете SDK DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) заметки о выпуске для августа 2009 г. обновление платформы для Windows Vista

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[обновление платформы для Windows Vista](platform-update-for-windows-vista-portal.md)
</dt> <dt>

**Разделы общих сведений**
</dt> <dt>

[сведения об обновлении платформы для Windows Vista](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[статья базы знаний об обновлении платформы для Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 