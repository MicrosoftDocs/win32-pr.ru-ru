---
title: Метод Иделиверйоптимизатионжоб Аддфилевисранжес (Deliveryoptimization. h)
description: Добавляет файл в задание загрузки и задает диапазоны файлов, которые необходимо загрузить.
ms.assetid: 23F0A39F-670F-4030-A3B3-4F9277FFA8AB
keywords:
- Метод Аддфилевисранжес
- Метод Аддфилевисранжес, интерфейс Иделиверйоптимизатионжоб
- Интерфейс Иделиверйоптимизатионжоб, метод Аддфилевисранжес
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob.AddFileWithRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 197aa7443123c81d1a675d321b91573823a84f15
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476134"
---
# <a name="ideliveryoptimizationjobaddfilewithranges-method"></a>Метод Иделиверйоптимизатионжоб:: Аддфилевисранжес

Добавляет файл в задание загрузки и задает диапазоны файлов, которые необходимо загрузить.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AddFileWithRanges(
  [in]           LPCWSTR       fileId,
  [in]           LPCWSTR       remoteUrl,
  [in]           LPCWSTR       localName,
  [in, optional] DWORD         rangeCount,
  [in, optional] BG_FILE_RANGE ranges[],
  [in, optional] ULONG64       fileSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ИД* \[ для окне\]
</dt> <dd>

Строка, заканчивающаяся нулем, которая является уникальным идентификатором опубликованного содержимого. Для неопубликованного содержимого это может быть любая уникальная строка, которую вызывающий объект может использовать для идентификации файлов в задании.

</dd> <dt>

*ремотеурл* \[ окне\]
</dt> <dd>

Строка, заканчивающаяся нулем и содержащая имя файла на сервере.

</dd> <dt>

*LocalName* \[ окне\]
</dt> <dd>

Строка, заканчивающаяся нулем и содержащая имя файла на клиенте.

</dd> <dt>

*ранжекаунт* \[ в необязательное\]
</dt> <dd>

Число элементов в *диапазонах*.

</dd> <dt>

*диапазоны* \[ в необязательное\]
</dt> <dd>

Массив из одной или нескольких структур [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) , указывающих диапазоны для загрузки. Не указывайте дублирующиеся или перекрывающиеся диапазоны.

</dd> <dt>

*Размер файла* \[ в необязательное\]
</dt> <dd>

Размер файла в байтах. Передайте **DO_UNKNOWN_FILE_SIZE** , если размер не известен вызывающему приложению.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает следующие возвращаемые значения, а также другие.




| Код возврата | Описание | 
|-------------|-------------|
| <dl><dt><strong><strong>S_OK</strong></strong></dt></dl> | Успешно.<br /> | 
| <dl><dt><strong>E_INVALIDARG</strong></dt></dl> | Имя локального файла имеет значение NULL или является пустой строкой. <br /> | 
| <dl><dt><strong>E_ACCESSDENIED</strong></dt></dl> | У пользователя нет разрешения на запись в указанный каталог на клиенте.<br /> | 
| <dl><dt><strong>DO_E_INVALID_RANGE</strong></dt></dl> | Один из диапазонов недопустим. Например, Инитиалоффсет имеет значение <strong>BG_LENGTH_TO_EOF</strong>.<br /> | 
| <dl><dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt></dl> | Нельзя указывать дублирующиеся или перекрывающиеся диапазоны. <br /><blockquote>[!Note]<br />Диапазоны сортируются по смещению значения, а не к длине. Если введены диапазоны с одинаковым смещением, но находятся в обратном порядке, возвращается эта ошибка. Например, если в этом порядке введены 100,5 и 100,0, вы не сможете добавить файл в задание.</blockquote><br /> | 
| <dl><dt><strong>DO_E_INVALID_STATE</strong></dt></dl> | Состояние задания не может быть <strong>BG_JOB_STATE_CANCELLED</strong> или <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>.<br /> | 




 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Server, только для \[ настольных приложений версии 1709\]<br/>                                       |
| Заголовок<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob определяется как EE2584CF-A69C-4848-B633-2649962B3EF7<br/>         |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иделиверйоптимизатионжоб**](ideliveryoptimizationjob.md)
</dt> </dl>

 

