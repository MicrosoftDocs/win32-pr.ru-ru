---
title: IMsRdpClientAdvancedSettings5 Аудиоредиректионмоде, свойство
description: Задает и получает режим перенаправления звука и различные параметры перенаправления звука.
ms.assetid: c0f5762b-00fd-40bb-ac97-3351b999f38d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Аудиоредиректионмоде
- Службы удаленных рабочих столов свойства Аудиоредиректионмоде, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Аудиоредиректионмоде
- Службы удаленных рабочих столов свойства Аудиоредиректионмоде, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Аудиоредиректионмоде
- Службы удаленных рабочих столов свойства Аудиоредиректионмоде, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Аудиоредиректионмоде
- Службы удаленных рабочих столов свойства Аудиоредиректионмоде, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Аудиоредиректионмоде
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.AudioRedirectionMode
- IMsRdpClientAdvancedSettings5.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings5.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df4216b4babf74e5e5f15994c0d8387e0d5087c4f69e4d0245b59cb5765dfe88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118352516"
---
# <a name="imsrdpclientadvancedsettings5audioredirectionmode-property"></a>Свойство IMsRdpClientAdvancedSettings5:: Аудиоредиректионмоде

Задает и получает режим перенаправления звука и различные параметры перенаправления звука.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_AudioRedirectionMode(
  [in]  UINT uiAudioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] UINT *puiAudioRedirectionMode
);
```



## <a name="property-value"></a>Значение свойства

Задает различные значения для режима перенаправления звука. Этот параметр имеет следующие возможные значения.

<dt>

<span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span>

**Звуковые \_ файлы РЕЖИМ \_ перенаправления 0** (перенаправление звука включено, а параметр перенаправления — "перенаправление на этот компьютер"). Это режим по умолчанию.)


</dt> <dd></dd> <dt>

<span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span>

**Звуковые \_ файлы РЕЖИМ \_ воспроизведения \_ на \_ сервере 1** (включено перенаправление звука, а параметр — "оставить на удаленном компьютере"). параметр "оставить на удаленном компьютере" поддерживается только при удаленном подключении к главному компьютеру, на котором работает Windows Vista. если подключение установлено к главному компьютеру, на котором работает Windows Server 2008, параметр "оставить на удаленном компьютере" изменится на "не воспроизводить".)


</dt> <dd></dd> <dt>

<span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span>

**Звуковые \_ файлы РЕЖИМ \_ нет 2** (перенаправление звука включено, а режим — "не воспроизводить").


</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                         |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                   |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings5 определяется как FBA7F64E-6783-4405-DA45-FA4A763DABD0<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





