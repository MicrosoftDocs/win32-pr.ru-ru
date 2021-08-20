---
description: Метод PATCH. Саурцелистаддмедиадиск. метод Саурцелистаддмедиадиск добавляет диск к набору зарегистрированных дисков. Принимает параметры DiskID, VolumeLabel и DiskPrompt в качестве параметров. Этот метод вызывает в Мсисаурцелистаддмедиадиск.
ms.assetid: 6feaf2d3-7e39-4e22-9e74-9a2f98369eac
title: Метод PATCH. Саурцелистаддмедиадиск
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3df81274581c64a37fbf505bbfd68d0907f5ca626e58bdfccbac61156fd29a9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942615"
---
# <a name="patchsourcelistaddmediadisk-method"></a>Метод PATCH. Саурцелистаддмедиадиск

Метод **саурцелистаддмедиадиск** добавляет диск к набору зарегистрированных дисков. Принимает параметры *DiskID*, *VolumeLabel* и *DiskPrompt* в качестве параметров. Этот метод вызывает в [**мсисаурцелистаддмедиадиск**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).

## <a name="syntax"></a>Синтаксис


```JScript
Patch.SourceListAddMediaDisk(
  Diskid,
  VolumeLabel,
  DiskPrompt
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*DiskID* 
</dt> <dd>

Этот параметр задает идентификатор добавляемого или обновляемого диска.

</dd> <dt>

*VolumeLabel* 
</dt> <dd>

Этот параметр задает метку добавляемого или обновляемого диска. Обновление перезаписывает существующую метку тома в реестре. Чтобы изменить только приглашение на диск, получите имеющуюся метку зарегистрированного тома и укажите ее вместе с новым диском. Значение NULL или пустая строка регистрирует пустую строку (длиной 0 байт) в качестве метки тома.

</dd> <dt>

*DiskPrompt* 
</dt> <dd>

Этот параметр позволяет ввести в диск запрос на добавление или обновление диска. Обновление перезаписывает существующий диск в реестре. Чтобы изменить только метку тома, получите существующий дисковый запрос из реестра и укажите для него новую метку тома. Значение NULL или пустая строка регистрирует пустую строку (длиной 0 байт) в качестве запроса диска.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик 3,0 или более поздней версии на Windows Server 2003, Windows XP и Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ ипатч определен как 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Обновление**](patch-object.md)
</dt> <dt>

[**мсисаурцелистаддмедиадиск**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




