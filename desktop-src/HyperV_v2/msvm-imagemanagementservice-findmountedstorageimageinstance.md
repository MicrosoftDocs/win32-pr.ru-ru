---
description: Находит \_ объект Маунтедсторажеимаже мсвм для указанного пути к образу диска.
ms.assetid: 498ed285-2b5b-472b-b0ee-649c97b61274
title: Метод Финдмаунтедсторажеимажеинстанце класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.FindMountedStorageImageInstance
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80462fb57be8c3f89764774ea68e73a988f11643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542471"
---
# <a name="findmountedstorageimageinstance-method-of-the-msvm_imagemanagementservice-class"></a>Метод Финдмаунтедсторажеимажеинстанце \_ класса) мсвм

Находит объект [**\_ маунтедсторажеимаже мсвм**](msvm-mountedstorageimage.md) для указанного пути к образу диска.

## <a name="syntax"></a>Синтаксис


```mof
uint32 FindMountedStorageImageInstance(
  [in]  string                       SelectionCriterion,
  [in]  uint16                       CriterionType,
  [out] Msvm_MountedStorageImage REF Image
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Селектионкритерион* \[ окне\]
</dt> <dd>

Полный путь, указывающий расположение файла образа диска.

</dd> <dt>

*Критерионтипе* \[ окне\]
</dt> <dd>

Тип критерия, который нужно найти при поиске образа диска.

<dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

**неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>

**Путь** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*Изображение* \[ заполняет\]
</dt> <dd>

Ссылка на [**\_ маунтедсторажеимаже мсвм**](msvm-mountedstorageimage.md) (может иметь значение null, если образ не подключен).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает одно из следующих значений:

<dl> <dt>

**Завершено без ошибок** (0)
</dt> <dt>

**Сбой** (32768)
</dt> <dt>

**Отказано в доступе** (32769)
</dt> <dt>

**Не поддерживается** (32770)
</dt> <dt>

**Состояние неизвестно** (32771)
</dt> <dt>

**Время ожидания** (32772)
</dt> <dt>

**Недопустимый параметр** (32773)
</dt> <dt>

**Система используется** (32774)
</dt> <dt>

**Недопустимое состояние для этой операции** (32775)
</dt> <dt>

**Неверный тип данных** (32776)
</dt> <dt>

**Система недоступна** (32777)
</dt> <dt>

**Недостаточно памяти** (32778)
</dt> <dt>

**Файл не найден** (32779)
</dt> <dt>

**Объект не найден** (32789)
</dt> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ )**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




