---
description: Метод Product. Саурцелистаддмедиадиск — метод Саурцелистаддмедиадиск добавляет диск к набору зарегистрированных дисков. Принимает параметры DiskID, VolumeLabel и DiskPrompt в качестве параметров. Этот метод вызывает в Мсисаурцелистаддмедиадиск.
ms.assetid: 19cb6884-2191-4da3-a6d2-8874564be67d
title: Метод Product. Саурцелистаддмедиадиск
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4cf5fac906b048930b47a07acb2c04c7243d5bbf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113582"
---
# <a name="productsourcelistaddmediadisk-method"></a>Метод Product. Саурцелистаддмедиадиск

Метод **саурцелистаддмедиадиск** добавляет диск к набору зарегистрированных дисков. Принимает параметры *DiskID*, *VolumeLabel* и *DiskPrompt* в качестве параметров. Этот метод вызывает в [**мсисаурцелистаддмедиадиск**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).

## <a name="syntax"></a>Синтаксис


```JScript
Product.SourceListAddMediaDisk(
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

Этот параметр задает метку добавляемого или обновляемого диска. Обновление перезаписывает существующую метку тома в реестре. Чтобы изменить только приглашение на диск, получите имеющуюся метку зарегистрированного тома и укажите ее вместе с новым диском. Пустая строка для этого параметра регистрирует пустую строку (в длину 0 байт) в качестве метки тома.

</dd> <dt>

*DiskPrompt* 
</dt> <dd>

Этот параметр позволяет ввести в диск запрос на добавление или обновление диска. Обновление перезаписывает существующий диск в реестре. Чтобы изменить только метку тома, получите существующий дисковый запрос из реестра и укажите для него новую метку тома. Пустая строка для этого параметра регистрирует пустую строку (в длину 0 байт) в качестве запроса диска.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ ипродукт определен как 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Продукта**](product-object.md)
</dt> <dt>

[**мсисаурцелистаддмедиадиск**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[Не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




