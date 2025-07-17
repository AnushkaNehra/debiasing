first set up the virtual env for the python
then install the requirements for the env using the command pip install -r requirements
then add the model LLaMA2-7B chat vicuna for the evironmne tot tun on this is the model we currently working on and abide by this 
then clone the github repo of cal from the paper
then clone the github repo of trl for dpo from this github --> https://github.com/huggingface/trl
then to add the loss function do it in the trainer file of the dpo trainer trl and can start working on that 

this is the huuging face link for your original trained model --https://huggingface.co/Nehraanushka/llama2-chat-finetuned--  and u can access this model of your by this command line 

from transformers import AutoModelForCausalLM, AutoTokenizer
model = AutoModelForCausalLM.from_pretrained("Nehraanushka/llama2-chat-finetuned")
tokenizer = AutoTokenizer.from_pretrained("Nehraanushka/llama2-chat-finetuned")
inputs = tokenizer("Hello, how are you?", return_tensors="pt")
outputs = model.generate(**inputs)
print(tokenizer.decode(outputs[0], skip_special_tokens=True))


